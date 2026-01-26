<script lang="ts">
  let selectedService = 'mid-term';
</script>

<section class="bg-surface-light py-24 px-6">
  <div class="max-w-[1200px] mx-auto text-center">
    <h2 class="text-3xl md:text-4xl font-light text-gray-900 mb-16">
      Two service tiers. <span class="text-gray-400">Maximum flexibility.</span>
    </h2>

    <div class="mb-8">
      <h3 class="text-xl md:text-2xl font-medium mb-2">Mid-Term Rentals</h3>
      <p class="text-gray-500 text-sm">Stable, consistent income with 30+ day stays.</p>
    </div>

    <!-- Service Showcase -->
    <div class="relative w-full h-[400px] bg-white rounded-xl mb-8 flex items-center justify-center overflow-hidden shadow-sm">
      <div class="grid grid-cols-3 gap-8 p-12 w-full max-w-[800px]">
        <div class="text-center">
          <div class="w-16 h-16 mx-auto mb-4 bg-primary-50 rounded-full flex items-center justify-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-primary-600"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
          </div>
          <h4 class="font-medium text-sm mb-1">Professional Furnishing</h4>
          <p class="text-xs text-gray-500">High-end furniture & decor</p>
        </div>
        <div class="text-center">
          <div class="w-16 h-16 mx-auto mb-4 bg-primary-50 rounded-full flex items-center justify-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-primary-600"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
          </div>
          <h4 class="font-medium text-sm mb-1">Tenant Management</h4>
          <p class="text-xs text-gray-500">Full screening & support</p>
        </div>
        <div class="text-center">
          <div class="w-16 h-16 mx-auto mb-4 bg-primary-50 rounded-full flex items-center justify-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-primary-600"><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
          </div>
          <h4 class="font-medium text-sm mb-1">Guaranteed Income</h4>
          <p class="text-xs text-gray-500">Predictable monthly returns</p>
        </div>
      </div>
    </div>

    <!-- Service Toggle -->
    <div class="flex justify-center gap-4 mb-8">
      <button class="px-6 py-2 rounded-full {selectedService === 'mid-term' ? 'bg-primary-600 text-white' : 'bg-gray-200 text-gray-600'} text-sm font-medium transition-colors">
        Mid-Term Rentals
      </button>
      <button class="px-6 py-2 rounded-full {selectedService === 'short-term' ? 'bg-primary-600 text-white' : 'bg-gray-200 text-gray-600'} text-sm font-medium transition-colors">
        High-End Short-Term
      </button>
    </div>

    <div class="flex justify-center gap-8 text-sm text-gray-600 mb-4 border-b border-gray-200 pb-4 inline-flex mx-auto w-auto px-12">
      <span>30+ day stays</span>
      <span>Full furnishing</span>
      <span>100% managed</span>
    </div>

    <p class="text-sm text-gray-500 mb-8">
      Maximize your rental income with <span class="font-medium text-gray-900">professional management</span>.<br>
      Schedule a consultation to get your property's income projection.
    </p>

    <div class="flex flex-col sm:flex-row justify-center gap-4">
      <button class="px-6 py-3 bg-gray-100 hover:bg-gray-200 rounded-lg text-sm font-medium transition-colors duration-300 text-left">
        <span class="block text-xs text-gray-500">Learn more about</span>
        <span class="text-primary-600">Our services</span>
      </button>
      <button class="px-6 py-3 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors duration-300 flex items-center justify-center gap-2">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/></svg>
        Schedule consultation →
      </button>
    </div>
  </div>
</section>
