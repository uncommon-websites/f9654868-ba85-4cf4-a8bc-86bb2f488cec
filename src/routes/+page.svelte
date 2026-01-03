<script lang="ts">
  import TopBanner from "$lib/components/TopBanner.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import Hero from "$lib/components/Hero.svelte";
  import Intro from "$lib/components/Intro.svelte";
  import VideoExplainer from "$lib/components/VideoExplainer.svelte";
  import Carousel from "$lib/components/Carousel.svelte";
  import ValueProp from "$lib/components/ValueProp.svelte";
  import ShowroomGrid from "$lib/components/ShowroomGrid.svelte";
  import LifeWithBackyard from "$lib/components/LifeWithBackyard.svelte";
  import ProductConfigurator from "$lib/components/ProductConfigurator.svelte";
  import PeekInside from "$lib/components/PeekInside.svelte";
  import Steps from "$lib/components/Steps.svelte";
  import Features from "$lib/components/Features.svelte";
  import Illustration from "$lib/components/Illustration.svelte";
  import Sustainability from "$lib/components/Sustainability.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<div class="font-sans antialiased text-gray-900 bg-white">
  <TopBanner />
  <Navbar />
  <main>
    <Hero />
    <Intro />
    <VideoExplainer 
      videoId="toMhkoSW86Q"
      title="Understanding mid-term rentals"
      description="Learn how FredPM maximizes your rental income through strategic mid-term property management."
    />
    <Carousel />
    <ValueProp />
    <ShowroomGrid />
    <LifeWithBackyard />
    <ProductConfigurator />
    <PeekInside />
    <Steps />
    <Features />
    <Illustration />
    <Sustainability />
  </main>
  <Footer />
</div>

