<script lang="ts">
  import { onMount } from 'svelte';

  let mounted = $state(false);

  onMount(() => {
    setTimeout(() => {
      mounted = true;
    }, 100);
  });
</script>

<section class="min-h-screen bg-surface relative overflow-hidden">
  <!-- Background Image -->
  <div class="absolute inset-0">
    <img
      src="/generated/image-modern-luxury-furnished-apartment-living-1767220468619-0.webp"
      alt="Luxury furnished rental property"
      class="w-full h-full object-cover"
    />
    <div class="absolute inset-0 bg-black/40"></div>
  </div>

  <!-- Content -->
  <div class="relative z-10 min-h-screen flex flex-col">
    <!-- Main Content -->
    <div class="flex-1 flex flex-col items-center justify-center px-6 text-center">
      <div
        class="transition-all duration-700 ease-out"
        style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 30}px);"
      >
        <h1 class="text-5xl md:text-7xl lg:text-8xl font-light text-white tracking-tight mb-6">
          FredPM
        </h1>
        <p class="text-xl md:text-2xl text-white/80 font-light mb-4 max-w-2xl mx-auto">
          Premium Property Management
        </p>
        <p class="text-lg text-white/60 mb-12">
          How can we help you today?
        </p>
      </div>

      <!-- Dual Entry Buttons -->
      <div
        class="flex flex-col sm:flex-row gap-4 sm:gap-6 transition-all duration-700 ease-out"
        style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 20}px); transition-delay: 200ms;"
      >
        <a
          href="/guests"
          class="group relative px-10 py-5 bg-white text-gray-900 rounded-lg text-lg font-medium hover:bg-gray-50 transition-all duration-300 shadow-lg hover:shadow-xl min-w-[280px]"
        >
          <span class="block text-sm text-gray-500 mb-1">I'm looking to</span>
          <span class="block text-xl">Find a Rental</span>
          <span class="absolute right-6 top-1/2 -translate-y-1/2 text-gray-400 group-hover:translate-x-1 transition-transform duration-300">→</span>
        </a>

        <a
          href="/owners"
          class="group relative px-10 py-5 bg-primary-500 text-white rounded-lg text-lg font-medium hover:bg-primary-600 transition-all duration-300 shadow-lg hover:shadow-xl min-w-[280px]"
        >
          <span class="block text-sm text-white/70 mb-1">I'm a</span>
          <span class="block text-xl">Property Owner</span>
          <span class="absolute right-6 top-1/2 -translate-y-1/2 text-white/70 group-hover:translate-x-1 transition-transform duration-300">→</span>
        </a>
      </div>
    </div>

    <!-- Bottom indicator -->
    <div
      class="pb-8 text-center transition-all duration-700 ease-out"
      style="opacity: {mounted ? 1 : 0}; transition-delay: 500ms;"
    >
      <p class="text-white/50 text-sm">Scroll to explore</p>
      <div class="mt-2 w-6 h-10 border-2 border-white/30 rounded-full mx-auto flex justify-center">
        <div class="w-1 h-2 bg-white/50 rounded-full mt-2 animate-bounce"></div>
      </div>
    </div>
  </div>
</section>
