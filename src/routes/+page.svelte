<script lang="ts">
  import TopBanner from "$lib/components/TopBanner.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import HeroEntry from "$lib/components/HeroEntry.svelte";
  import Intro from "$lib/components/Intro.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<div class="font-sans antialiased text-gray-900 bg-white">
  <TopBanner />
  <Navbar />
  <main>
    <HeroEntry />
    <Intro />
  </main>
  <Footer />
</div>
