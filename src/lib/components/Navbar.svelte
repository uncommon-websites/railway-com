<script lang="ts">
  import { onMount } from 'svelte';

  let scrolled = false;

  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 20;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<nav class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 border-b border-transparent {scrolled ? 'bg-[#0b0c0e]/80 backdrop-blur-md border-[#2e3036]' : 'bg-transparent'}">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16">
      <!-- Logo -->
      <div class="flex-shrink-0 flex items-center">
        <a href="/" class="flex items-center gap-2 group">
          <svg viewBox="0 0 24 24" fill="none" class="w-8 h-8 text-white" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 2L2 19H22L12 2Z" fill="currentColor" class="group-hover:text-purple-500 transition-colors duration-300"/>
            <path d="M12 6L5.5 17H18.5L12 6Z" fill="#0b0c0e"/>
          </svg>
          <span class="text-xl font-bold tracking-tight">Railway</span>
        </a>
      </div>

      <!-- Links -->
      <div class="hidden md:flex items-center space-x-8">
        <a href="#" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Product</a>
        <a href="#" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Developers</a>
        <a href="#" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Enterprise</a>
        <a href="#" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Company</a>
        <a href="#" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Pricing</a>
      </div>

      <!-- Actions -->
      <div class="hidden md:flex items-center space-x-4">
        <a href="#" class="text-sm font-medium text-white hover:text-gray-300 transition-colors">Sign in</a>
        <a href="#" class="text-sm font-medium px-4 py-2 rounded-full border border-gray-700 hover:bg-gray-800 transition-colors">Book a demo</a>
      </div>

      <!-- Mobile menu button -->
      <div class="md:hidden flex items-center">
        <button class="text-gray-300 hover:text-white p-2">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>
    </div>
  </div>
</nav>
