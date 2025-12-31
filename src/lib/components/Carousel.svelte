<script lang="ts">
  const images = [
    "/generated/image-modern-luxury-furnished-apartment-living-1767220468619-0.webp",
    "/generated/image-upscale-modern-apartment-interior-with-o-1767220483867-5.webp",
    "/generated/image-luxury-living-room-with-comfortable-sofa-1767220486649-6.webp"
  ];
</script>

<section class="bg-white pb-24 overflow-hidden" id="properties">
  <div class="flex gap-4 overflow-x-auto px-6 pb-8 snap-x">
    {#each images as img}
      <div class="min-w-[80vw] md:min-w-[60vw] lg:min-w-[45vw] h-[400px] snap-center first:pl-0">
        <img src={img} alt="Managed property" class="w-full h-full object-cover rounded-lg" />
      </div>
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
