<script lang="ts">
  import TopBanner from "$lib/components/TopBanner.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import Carousel from "$lib/components/Carousel.svelte";
  import ShowroomGrid from "$lib/components/ShowroomGrid.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import { onMount } from 'svelte';

  let mounted = $state(false);

  onMount(() => {
    setTimeout(() => {
      mounted = true;
    }, 100);
  });
</script>

<div class="font-sans antialiased text-gray-900 bg-white">
  <TopBanner />
  <Navbar />

  <main>
    <!-- Guest Hero -->
    <section class="bg-surface pt-20 pb-16">
      <div class="max-w-[1200px] mx-auto px-6">
        <div
          class="text-center max-w-3xl mx-auto transition-all duration-700 ease-out"
          style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 30}px);"
        >
          <p class="text-primary-500 font-medium mb-4">For Guests</p>
          <h1 class="text-4xl md:text-6xl font-light tracking-tight mb-6">
            Find Your Perfect Stay
          </h1>
          <p class="text-xl text-gray-600 mb-8">
            Discover beautifully furnished rentals for your mid-term or short-term stay.
            Professional service, transparent pricing, real people.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <a
              href="#properties"
              class="px-8 py-4 bg-primary-500 text-white rounded-lg font-medium hover:bg-primary-600 transition-colors duration-300"
            >
              Browse Properties
            </a>
            <a
              href="#contact"
              class="px-8 py-4 bg-gray-100 text-gray-900 rounded-lg font-medium hover:bg-gray-200 transition-colors duration-300"
            >
              Contact Us
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Why Choose Us -->
    <section class="bg-surface-light py-20">
      <div class="max-w-[1200px] mx-auto px-6">
        <h2 class="text-3xl md:text-4xl font-light text-center mb-12">Why Stay With FredPM?</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="text-center p-6">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-medium mb-2">Verified Properties</h3>
            <p class="text-gray-600">Every property is professionally inspected and maintained to our high standards.</p>
          </div>
          <div class="text-center p-6">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-medium mb-2">Transparent Pricing</h3>
            <p class="text-gray-600">No hidden fees. What you see is what you pay, all-inclusive pricing.</p>
          </div>
          <div class="text-center p-6">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-medium mb-2">24/7 Support</h3>
            <p class="text-gray-600">Real people available around the clock to help with anything you need.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Properties Section -->
    <section id="properties">
      <Carousel />
    </section>

    <!-- Featured Properties Grid -->
    <ShowroomGrid />

    <!-- CTA Section -->
    <section class="bg-primary-500 py-20">
      <div class="max-w-[1200px] mx-auto px-6 text-center">
        <h2 class="text-3xl md:text-4xl font-light text-white mb-4">Ready to Book Your Stay?</h2>
        <p class="text-xl text-white/80 mb-8">Browse our available properties or get in touch for personalized recommendations.</p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="#properties"
            class="px-8 py-4 bg-white text-primary-600 rounded-lg font-medium hover:bg-gray-100 transition-colors duration-300"
          >
            View All Properties
          </a>
          <a
            href="#contact"
            class="px-8 py-4 bg-primary-600 text-white rounded-lg font-medium hover:bg-primary-700 transition-colors duration-300 border border-white/20"
          >
            Contact Us
          </a>
        </div>
      </div>
    </section>
  </main>

  <Footer />
</div>
