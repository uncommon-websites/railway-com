<section class="py-32 border-t border-[#2e3036] bg-[#0b0c0e] relative overflow-hidden">
  <!-- Grid Background -->
  <div class="absolute inset-0 bg-[linear-gradient(to_right,#1c1d22_1px,transparent_1px),linear-gradient(to_bottom,#1c1d22_1px,transparent_1px)] bg-[size:24px_24px] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_0%,#000_70%,transparent_100%)] pointer-events-none"></div>

  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
    <h2 class="text-3xl md:text-5xl font-bold text-white mb-4">17.9M+ deploys per month (and counting)</h2>
    <p class="text-gray-400 mb-16">Real-time usage showing totals for users and services, along with 30-day deploys, requests, and logs.</p>

    <div class="max-w-4xl mx-auto space-y-6 font-mono text-lg md:text-xl">
       <!-- Users -->
       <div class="flex flex-col md:flex-row justify-between items-center border-b border-gray-800 pb-4 gap-4">
          <span class="text-gray-500 tracking-[0.3em] uppercase text-sm w-full md:w-auto text-left">Users</span>
          <div class="flex gap-1">
             {#each "1,960,030".split('') as char}
               <div class="w-6 h-9 md:w-8 md:h-10 bg-[#131418] border border-[#2e3036] rounded flex items-center justify-center text-white shadow-inner">
                 {char}
               </div>
             {/each}
          </div>
       </div>
       <!-- Services -->
       <div class="flex flex-col md:flex-row justify-between items-center border-b border-gray-800 pb-4 gap-4">
          <span class="text-gray-500 tracking-[0.3em] uppercase text-sm w-full md:w-auto text-left">Services</span>
          <div class="flex gap-1">
             {#each "5,761,660".split('') as char}
               <div class="w-6 h-9 md:w-8 md:h-10 bg-[#131418] border border-[#2e3036] rounded flex items-center justify-center text-white shadow-inner">
                 {char}
               </div>
             {/each}
          </div>
       </div>
       <!-- Deploys -->
       <div class="flex flex-col md:flex-row justify-between items-center border-b border-gray-800 pb-4 gap-4">
          <span class="text-gray-500 tracking-[0.3em] uppercase text-sm w-full md:w-auto text-left">Deploys</span>
          <div class="flex gap-1">
             {#each "17,910,558".split('') as char}
               <div class="w-6 h-9 md:w-8 md:h-10 bg-[#131418] border border-[#2e3036] rounded flex items-center justify-center text-white shadow-inner">
                 {char}
               </div>
             {/each}
          </div>
       </div>
       <!-- Requests -->
       <div class="flex flex-col md:flex-row justify-between items-center border-b border-gray-800 pb-4 gap-4">
          <span class="text-gray-500 tracking-[0.3em] uppercase text-sm w-full md:w-auto text-left">Requests</span>
          <div class="flex gap-1">
             {#each "70,837,732,275".split('') as char}
               <div class="w-6 h-9 md:w-8 md:h-10 bg-[#131418] border border-[#2e3036] rounded flex items-center justify-center text-white shadow-inner">
                 {char}
               </div>
             {/each}
          </div>
       </div>
       <!-- Logs -->
       <div class="flex flex-col md:flex-row justify-between items-center border-b border-gray-800 pb-4 gap-4">
          <span class="text-gray-500 tracking-[0.3em] uppercase text-sm w-full md:w-auto text-left">Logs</span>
          <div class="flex gap-1">
             {#each "289,863,900,679".split('') as char}
               <div class="w-6 h-9 md:w-8 md:h-10 bg-[#131418] border border-[#2e3036] rounded flex items-center justify-center text-white shadow-inner">
                 {char}
               </div>
             {/each}
          </div>
       </div>
    </div>
  </div>
</section>
