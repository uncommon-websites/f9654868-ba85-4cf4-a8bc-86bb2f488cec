<script lang="ts">
  import { onMount } from 'svelte';

  let sectionEl: HTMLElement;
  let isVisible = $state(false);

  onMount(() => {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            isVisible = true;
            observer.unobserve(sectionEl);
          }
        });
      },
      { threshold: 0.2 }
    );

    observer.observe(sectionEl);
    return () => observer.disconnect();
  });
</script>

<section bind:this={sectionEl} class="bg-surface py-24 px-6">
  <div class="max-w-[1000px] mx-auto text-center">
    <h2
      class="text-4xl md:text-5xl leading-[1.1] font-light tracking-tight text-gray-900 mb-12 transition-all duration-700 ease-out"
      style="opacity: {isVisible ? 1 : 0}; transform: translateY({isVisible ? 0 : 30}px);"
    >
      FredPM
      <span class="inline-flex items-center justify-center align-middle mx-1 bg-gray-100 rounded-lg px-2 h-12 w-16">
        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-gray-800"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
      </span>
      delivers<br>
      full-service, hassle-free<br>
      property management
      <span class="inline-flex items-center justify-center align-middle mx-1 bg-gray-100 rounded-lg px-2 h-12 w-14">
        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-gray-800"><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
      </span>
      with<br>
      maximum
      <span class="inline-flex items-center justify-center align-middle mx-1 bg-gray-100 rounded-lg px-2 h-12 w-16">
        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-gray-800"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
      </span>
      rental income.
    </h2>

    <p
      class="text-gray-500 text-lg mb-6 transition-all duration-700 ease-out"
      style="opacity: {isVisible ? 1 : 0}; transform: translateY({isVisible ? 0 : 20}px); transition-delay: 200ms;"
    >
      From professional furnishing to tenant management,<br>
      we handle everything so you can earn passive income.
    </p>

    <a
      href="#contact"
      class="text-sm text-gray-400 hover:text-gray-600 transition-all duration-300 group inline-flex items-center gap-1"
      style="opacity: {isVisible ? 1 : 0}; transition-delay: 400ms;"
    >
      Schedule a consultation <span class="group-hover:translate-x-1 transition-transform duration-300">→</span>
    </a>
  </div>
</section>
