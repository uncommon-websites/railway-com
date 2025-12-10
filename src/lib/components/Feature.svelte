<script lang="ts">
  export let title: string;
  export let headline: string;
  export let description: string;
  export let align: 'left' | 'right' = 'left';
  export let color: 'purple' | 'blue' | 'cyan' | 'green' = 'purple';

  const colorClasses = {
    purple: {
      text: 'text-purple-500',
      bg: 'bg-purple-500',
      hover: 'hover:text-purple-400',
      gradient: 'from-purple-500',
      shadow: 'shadow-purple-500/50'
    },
    blue: {
      text: 'text-blue-500',
      bg: 'bg-blue-500',
      hover: 'hover:text-blue-400',
      gradient: 'from-blue-500',
      shadow: 'shadow-blue-500/50'
    },
    cyan: {
      text: 'text-cyan-500',
      bg: 'bg-cyan-500',
      hover: 'hover:text-cyan-400',
      gradient: 'from-cyan-500',
      shadow: 'shadow-cyan-500/50'
    },
    green: {
      text: 'text-green-500',
      bg: 'bg-green-500',
      hover: 'hover:text-green-400',
      gradient: 'from-green-500',
      shadow: 'shadow-green-500/50'
    }
  };

  $: colors = colorClasses[color];
</script>

<section class="relative py-24 overflow-hidden">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
      
      <!-- Text Content -->
      <div class="{align === 'right' ? 'lg:order-2' : ''}">
        <div class="relative pl-8 border-l border-gray-800">
           <!-- Timeline dot/glow -->
           <div class="absolute -left-[5px] top-0 w-2.5 h-2.5 rounded-full {colors.bg} {colors.shadow} shadow-[0_0_15px]"></div>
           <div class="absolute -left-[1px] top-0 bottom-0 w-[1px] bg-gradient-to-b {colors.gradient} to-transparent opacity-50"></div>
           
           <h3 class="{colors.text} font-medium mb-4 tracking-wide uppercase text-sm">{title}</h3>
           <h2 class="text-3xl md:text-4xl font-bold text-white mb-6 leading-tight">{headline}</h2>
           <p class="text-gray-400 text-lg mb-8 leading-relaxed">
             {description}
           </p>
           
           <slot name="stats" />
           
           <a href="#" class="inline-flex items-center text-white font-medium {colors.hover} transition-colors mt-4">
             Learn More <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" /></svg>
           </a>
        </div>
      </div>

      <!-- Visual Content -->
      <div class="{align === 'right' ? 'lg:order-1' : ''}">
        <div class="relative rounded-xl border border-[#2e3036] bg-[#0b0c0e] overflow-hidden shadow-2xl group min-h-[400px]">
           <div class="absolute inset-0 bg-gradient-to-br {colors.gradient} to-transparent opacity-5 pointer-events-none"></div>
           <slot name="visual" />
        </div>
      </div>

    </div>
  </div>
</section>
