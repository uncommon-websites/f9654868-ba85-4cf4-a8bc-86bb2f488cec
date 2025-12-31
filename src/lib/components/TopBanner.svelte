<script lang="ts">
  export let text = "Learn More";
  export let href = "#";
</script>

<div class="bg-black text-white text-[11px] font-medium py-3 px-4 flex justify-between items-center tracking-wide">
  <div class="flex-1 text-center">
    <span class="opacity-90">Now managing properties in major metropolitan areas • Guaranteed income projections available</span>
  </div>
  <a {href} class="bg-primary-600 hover:bg-primary-700 text-white px-3 py-1.5 rounded text-[10px] font-bold uppercase tracking-wider ml-4 transition-colors">
    {text}
  </a>
</div>
