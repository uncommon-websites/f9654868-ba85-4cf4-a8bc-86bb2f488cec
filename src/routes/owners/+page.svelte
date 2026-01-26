<script lang="ts">
  import TopBanner from "$lib/components/TopBanner.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import VideoExplainer from "$lib/components/VideoExplainer.svelte";
  import Steps from "$lib/components/Steps.svelte";
  import Features from "$lib/components/Features.svelte";
  import ValueProp from "$lib/components/ValueProp.svelte";
  import ProductConfigurator from "$lib/components/ProductConfigurator.svelte";
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
    <!-- Owner Hero -->
    <section class="bg-surface pt-20 pb-16">
      <div class="max-w-[1200px] mx-auto px-6">
        <div
          class="text-center max-w-3xl mx-auto transition-all duration-700 ease-out"
          style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 30}px);"
        >
          <p class="text-primary-500 font-medium mb-4">For Property Owners</p>
          <h1 class="text-4xl md:text-6xl font-light tracking-tight mb-6">
            Maximize Your Rental Income
          </h1>
          <p class="text-xl text-gray-600 mb-8">
            Full-service property management for mid-term and high-end short-term rentals.
            Let us handle everything while you earn more.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <a
              href="#get-started"
              class="px-8 py-4 bg-primary-500 text-white rounded-lg font-medium hover:bg-primary-600 transition-colors duration-300"
            >
              Get Started
            </a>
            <a
              href="#learn-more"
              class="px-8 py-4 bg-gray-100 text-gray-900 rounded-lg font-medium hover:bg-gray-200 transition-colors duration-300"
            >
              Learn More
            </a>
          </div>
        </div>
      </div>

      <!-- Stats -->
      <div
        class="max-w-[1000px] mx-auto px-6 mt-16 transition-all duration-700 ease-out"
        style="opacity: {mounted ? 1 : 0}; transform: translateY({mounted ? 0 : 20}px); transition-delay: 200ms;"
      >
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
          <div>
            <p class="text-4xl md:text-5xl font-light text-primary-500">95%</p>
            <p class="text-gray-600 mt-2">Occupancy Rate</p>
          </div>
          <div>
            <p class="text-4xl md:text-5xl font-light text-primary-500">30%</p>
            <p class="text-gray-600 mt-2">More Revenue</p>
          </div>
          <div>
            <p class="text-4xl md:text-5xl font-light text-primary-500">500+</p>
            <p class="text-gray-600 mt-2">Properties Managed</p>
          </div>
          <div>
            <p class="text-4xl md:text-5xl font-light text-primary-500">24/7</p>
            <p class="text-gray-600 mt-2">Support</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Hero Image -->
    <div class="w-full h-[500px] bg-gray-100 overflow-hidden">
      <img
        src="/generated/image-modern-luxury-furnished-apartment-living-1767220468619-0.webp"
        alt="Luxury furnished rental property"
        class="w-full h-full object-cover"
      />
    </div>

    <!-- Video Section -->
    <section id="learn-more">
      <VideoExplainer
        videoId="toMhkoSW86Q"
        title="Why FredPM?"
        description="Learn how we maximize your rental income through strategic mid-term property management."
      />
    </section>

    <!-- Value Proposition -->
    <ValueProp />

    <!-- How It Works -->
    <Steps />

    <!-- Features -->
    <Features />

    <!-- Calculator/Configurator -->
    <section id="get-started">
      <ProductConfigurator />
    </section>

    <!-- CTA Section -->
    <section class="bg-gray-900 py-20">
      <div class="max-w-[1200px] mx-auto px-6 text-center">
        <h2 class="text-3xl md:text-4xl font-light text-white mb-4">Ready to Get Started?</h2>
        <p class="text-xl text-gray-400 mb-8">Join hundreds of property owners who trust FredPM to manage their rentals.</p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="#contact"
            class="px-8 py-4 bg-primary-500 text-white rounded-lg font-medium hover:bg-primary-600 transition-colors duration-300"
          >
            Schedule a Call
          </a>
          <a
            href="#calculator"
            class="px-8 py-4 bg-white/10 text-white rounded-lg font-medium hover:bg-white/20 transition-colors duration-300 border border-white/20"
          >
            Calculate Your Earnings
          </a>
        </div>
      </div>
    </section>
  </main>

  <Footer />
</div>
