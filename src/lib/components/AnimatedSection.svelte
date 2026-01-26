<script lang="ts">
  import { onMount } from 'svelte';

  type Props = {
    delay?: number;
    duration?: number;
    y?: number;
    once?: boolean;
    threshold?: number;
  };

  let {
    delay = 0,
    duration = 600,
    y = 30,
    once = true,
    threshold = 0.1
  }: Props = $props();

  let element: HTMLElement;
  let isVisible = $state(false);

  onMount(() => {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            isVisible = true;
            if (once) {
              observer.unobserve(element);
            }
          } else if (!once) {
            isVisible = false;
          }
        });
      },
      { threshold }
    );

    observer.observe(element);

    return () => observer.disconnect();
  });
</script>

<div
  bind:this={element}
  class="transition-all ease-out"
  style="
    opacity: {isVisible ? 1 : 0};
    transform: translateY({isVisible ? 0 : y}px);
    transition-duration: {duration}ms;
    transition-delay: {delay}ms;
  "
>
  <slot />
</div>
