<script lang="ts">
  type Props = {
    videoId?: string;
    title?: string;
    description?: string;
  };
  
  let { 
    videoId = 'dQw4w9WgXcQ', 
    title = 'Understanding mid-term rentals',
    description = 'Learn how FredPM maximizes your rental income through strategic mid-term property management.'
  }: Props = $props();
</script>

<section class="bg-white py-24 px-6">
  <div class="max-w-[1200px] mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-[48px] leading-tight font-light text-gray-900 mb-4">
        {title}
      </h2>
      <p class="text-gray-500 text-lg font-light max-w-[700px] mx-auto">
        {description}
      </p>
    </div>

    <div class="relative w-full" style="padding-bottom: 56.25%;">
      <iframe
        class="absolute top-0 left-0 w-full h-full rounded-lg shadow-sm"
        src={`https://www.youtube.com/embed/${videoId}`}
        title={title}
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</section>
