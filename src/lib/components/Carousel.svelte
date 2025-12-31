<script lang="ts">
  const properties = [
    {
      image: "/generated/image-modern-luxury-furnished-apartment-living-1767220468619-0.webp",
      url: "https://fredpm.holidayfuture.com"
    },
    {
      image: "/generated/image-upscale-modern-apartment-interior-with-o-1767220483867-5.webp",
      url: "https://fredpm.holidayfuture.com"
    },
    {
      image: "/generated/image-luxury-living-room-with-comfortable-sofa-1767220486649-6.webp",
      url: "https://fredpm.holidayfuture.com"
    }
  ];
</script>

<section class="bg-white pb-24 overflow-hidden" id="properties">
  <div class="flex gap-4 overflow-x-auto px-6 pb-8 snap-x">
    {#each properties as property}
      <a 
        href={property.url}
        target="_blank"
        rel="noopener noreferrer"
        class="min-w-[80vw] md:min-w-[60vw] lg:min-w-[45vw] h-[400px] snap-center first:pl-0 block group"
      >
        <div class="relative w-full h-full overflow-hidden rounded-lg">
          <img 
            src={property.image} 
            alt="Managed property" 
            class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" 
          />
          <div class="absolute inset-0 bg-black opacity-0 group-hover:opacity-10 transition-opacity duration-300"></div>
        </div>
      </a>
    {/each}
  </div>
  
  <div class="text-center mt-4">
    <p class="text-gray-500 text-sm mb-4">Mid-term & short-term rentals <span class="text-gray-400">professionally managed</span></p>
    <div class="flex justify-center gap-2">
      <div class="w-1.5 h-1.5 rounded-full bg-gray-800"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
    </div>
  </div>
</section>
