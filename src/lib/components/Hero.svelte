<script lang="ts">
  import { onMount } from 'svelte';

  let mounted = $state(false);

  onMount(() => {
    setTimeout(() => {
      mounted = true;
    }, 100);
  });
</script>

<section class="bg-surface pt-16 pb-0">
  <div class="max-w-[1200px] mx-auto px-6 mb-12">
    <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-start">
      <!-- Left -->
      <div
        class="md:col-span-3 pt-2 transition-all duration-700 ease-out"
        style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 20}px);"
      >
        <p class="text-gray-500 text-lg leading-tight">Maximize your<br>rental income.</p>
      </div>

      <!-- Center -->
      <div
        class="md:col-span-6 flex justify-center transition-all duration-700 ease-out"
        style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 30}px); transition-delay: 150ms;"
      >
        <h1 class="text-6xl md:text-8xl leading-none font-light tracking-tighter -mt-4">Full Service</h1>
      </div>

      <!-- Right -->
      <div
        class="md:col-span-3 pt-4 transition-all duration-700 ease-out"
        style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 20}px); transition-delay: 300ms;"
      >
        <p class="text-gray-600 text-sm leading-relaxed mb-4">
          Professional property management<br>
          for mid-term and high-end<br>
          short-term rentals.
        </p>
        <a href="#contact" class="text-sm font-medium text-gray-900 hover:text-gray-600 transition-colors duration-300 flex items-center gap-1 group">
          Get started <span class="text-xs group-hover:translate-x-1 transition-transform duration-300">→</span>
        </a>
      </div>
    </div>
  </div>

  <!-- Hero Image -->
  <div
    class="w-full h-[600px] bg-gray-100 overflow-hidden relative transition-all duration-1000 ease-out"
    id="hero-image"
    style="opacity: {mounted ? 1 : 0}; transform: scale({mounted ? 1 : 1.05}); transition-delay: 400ms;"
  >
    <img
      src="/generated/image-modern-luxury-furnished-apartment-living-1767220468619-0.webp"
      alt="Luxury furnished rental property"
      class="w-full h-full object-cover"
    />
  </div>
</section>
