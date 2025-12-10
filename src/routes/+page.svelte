<script lang="ts">
  import Navbar from '$lib/components/Navbar.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import LogoTicker from '$lib/components/LogoTicker.svelte';
  import Story from '$lib/components/Story.svelte';
  import Feature from '$lib/components/Feature.svelte';
  import Testimonials from '$lib/components/Testimonials.svelte';
  import Community from '$lib/components/Community.svelte';
  import Stats from '$lib/components/Stats.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<div class="bg-[#0b0c0e] min-h-screen text-white font-body selection:bg-purple-500/30">
  <Navbar />
  
  <main>
    <Hero />
    <LogoTicker />
    <Story />
    
    <!-- Feature 1: Build and Deploy -->
    <Feature 
      title="Build and Deploy"
      headline="Craft a complete full-stack application with a powerful visual canvas"
      description="Railway builds and deploys any combination of services, volumes, and databases from GitHub or Docker."
      color="purple"
      align="left"
    >
      <div slot="visual" class="w-full h-full min-h-[400px] bg-[#0b0c0e] p-6 relative">
         <!-- Mockup of Canvas -->
         <div class="absolute inset-0 bg-[radial-gradient(#1c1d22_1px,transparent_1px)] [background-size:16px_16px]"></div>
         
         <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 flex gap-8">
            <!-- Node 1 -->
            <div class="w-48 bg-[#131418] border border-[#2e3036] rounded p-3 shadow-lg">
               <div class="flex items-center gap-2 mb-2">
                  <div class="w-6 h-6 bg-white rounded flex items-center justify-center text-black text-xs font-bold">N</div>
                  <div class="text-xs font-medium">nextjs-app</div>
               </div>
               <div class="h-1 w-full bg-green-500 rounded-full mb-1"></div>
               <div class="text-[10px] text-gray-500">Deployed via GitHub</div>
            </div>
            
            <!-- Node 2 -->
            <div class="w-48 bg-[#131418] border border-[#2e3036] rounded p-3 shadow-lg mt-12">
               <div class="flex items-center gap-2 mb-2">
                  <div class="w-6 h-6 bg-[#336791] rounded flex items-center justify-center text-white text-xs font-bold">P</div>
                  <div class="text-xs font-medium">postgres</div>
               </div>
               <div class="h-1 w-full bg-green-500 rounded-full mb-1"></div>
               <div class="text-[10px] text-gray-500">Active</div>
            </div>
         </div>
         
         <!-- Connecting Line -->
         <svg class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-full h-full pointer-events-none" style="z-index: 0;">
             <path d="M260 200 L 300 200 L 300 250 L 340 250" stroke="#2e3036" stroke-width="1" fill="none" />
         </svg>
      </div>
    </Feature>

    <!-- Feature 2: Network and Connect -->
    <Feature 
      title="Network and Connect"
      headline="Interconnect your application seamlessly with highly performant networking"
      description="Railway provides automated service discovery, blazing fast networking, and support for any protocol, all out of the box."
      color="purple"
      align="left"
    >
      <div slot="stats" class="flex items-center gap-2 text-sm text-gray-400 mb-6">
         <svg class="w-5 h-5 text-purple-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" /></svg>
         <span class="text-white font-bold">50ms p95</span> global network RTT
      </div>
      <div slot="visual" class="w-full h-full min-h-[400px] bg-[#0b0c0e] p-6 relative flex items-center justify-center">
         <div class="absolute inset-0 bg-[radial-gradient(#1c1d22_1px,transparent_1px)] [background-size:16px_16px]"></div>
         
         <!-- Network Graph Mockup -->
         <div class="relative z-10 w-full h-full flex items-center justify-center">
            <!-- Nodes -->
            <div class="absolute top-1/4 left-1/4 transform -translate-x-1/2">
                <div class="bg-[#131418] border border-[#2e3036] p-2 rounded flex items-center gap-2 shadow-lg">
                    <div class="w-2 h-2 rounded-full bg-yellow-500"></div>
                    <span class="text-[10px] text-gray-300">frontend</span>
                </div>
            </div>
            
            <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
                <div class="bg-[#131418] border border-purple-500 p-2 rounded flex items-center gap-2 shadow-[0_0_15px_rgba(168,85,247,0.3)]">
                    <div class="w-2 h-2 rounded-full bg-purple-500"></div>
                    <span class="text-[10px] text-white">active-analytics</span>
                </div>
            </div>

            <div class="absolute bottom-1/4 right-1/4 transform translate-x-1/2">
                <div class="bg-[#131418] border border-[#2e3036] p-2 rounded flex items-center gap-2 shadow-lg">
                    <div class="w-2 h-2 rounded-full bg-blue-500"></div>
                    <span class="text-[10px] text-gray-300">postgres</span>
                </div>
            </div>
            
            <!-- Connecting Lines (SVG) -->
            <svg class="absolute inset-0 w-full h-full pointer-events-none" style="z-index: -1;">
                <path d="M 30% 30% L 50% 50%" stroke="#2e3036" stroke-width="1" stroke-dasharray="4 4" />
                <path d="M 50% 50% L 70% 70%" stroke="#2e3036" stroke-width="1" stroke-dasharray="4 4" />
                <circle cx="50%" cy="50%" r="60" stroke="#a855f7" stroke-width="1" fill="none" opacity="0.2" />
                <circle cx="50%" cy="50%" r="80" stroke="#a855f7" stroke-width="1" fill="none" opacity="0.1" />
            </svg>
         </div>
      </div>
    </Feature>

    <!-- Feature 3: Scale and Grow -->
    <Feature 
      title="Scale and Grow"
      headline="Scale your applications with intuitive vertical and horizontal scaling"
      description="Railway dynamically scales highly performant servers, storage, and networking to meet application demands."
      color="blue"
      align="right"
    >
      <div slot="stats" class="flex items-center gap-2 text-sm text-gray-400 mb-6">
         <svg class="w-5 h-5 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" /></svg>
         <span class="text-white font-bold">1000 vCPU</span> services
      </div>
      <div slot="visual" class="w-full h-full min-h-[400px] bg-[#0b0c0e] p-6 relative flex items-center justify-center">
         <div class="absolute inset-0 bg-[radial-gradient(#1c1d22_1px,transparent_1px)] [background-size:16px_16px]"></div>
         <div class="w-72 bg-[#131418] border border-[#2e3036] rounded-xl p-4 relative shadow-2xl">
            <!-- Badge -->
            <div class="absolute -top-3 -right-3 bg-pink-500 text-white text-[10px] font-bold px-2 py-1 rounded-full shadow-lg">16x</div>
            
            <div class="flex items-center gap-2 mb-6">
               <div class="w-8 h-8 rounded bg-white flex items-center justify-center text-black">
                  <svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2L2 7l10 5 10-5-10-5zm0 9l2.5-1.25L12 8.5l-2.5 1.25L12 11zm0 2.5l-5-2.5-5 2.5L12 22l10-8.5-5-2.5-5 2.5z"/></svg>
               </div>
               <div>
                  <div class="text-sm font-medium text-white">backend [US-West]</div>
                  <div class="text-[10px] text-green-400 flex items-center gap-1">
                     <div class="w-1.5 h-1.5 rounded-full bg-green-500"></div> Just deployed
                  </div>
               </div>
            </div>

            <div class="space-y-4">
               <div>
                  <div class="flex justify-between text-[10px] text-gray-400 mb-1">
                     <span>CPU Usage</span>
                     <span>64%</span>
                  </div>
                  <div class="h-1.5 bg-gray-800 rounded-full overflow-hidden">
                     <div class="h-full w-[64%] bg-blue-500 rounded-full"></div>
                  </div>
               </div>
               <div>
                  <div class="flex justify-between text-[10px] text-gray-400 mb-1">
                     <span>RAM Usage</span>
                     <span>32%</span>
                  </div>
                  <div class="h-1.5 bg-gray-800 rounded-full overflow-hidden">
                     <div class="h-full w-[32%] bg-purple-500 rounded-full"></div>
                  </div>
               </div>
            </div>
            
            <!-- Graph at bottom -->
            <div class="mt-6 h-24 flex items-end gap-1 opacity-50">
               {#each Array(16) as _, i}
                  <div class="w-full bg-blue-500/20 rounded-t" style="height: {20 + Math.random() * 60}%"></div>
               {/each}
            </div>
         </div>
      </div>
    </Feature>

    <!-- Feature 4: Monitor and Observe -->
    <Feature 
      title="Monitor and Observe"
      headline="Fix code faster with fully configurable observability"
      description="Railway provides precise logging, metrics, alerting, profiles, traces, and trend inspection without any code changes."
      color="purple"
      align="left"
    >
      <div slot="stats" class="flex items-center gap-2 text-sm text-gray-400 mb-6">
         <svg class="w-5 h-5 text-purple-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" /></svg>
         <span class="text-white font-bold">99.999%</span> enterprise SLAs
      </div>
      <div slot="visual" class="w-full h-full min-h-[400px] bg-[#0b0c0e] p-6 relative">
         <div class="absolute inset-0 bg-[radial-gradient(#1c1d22_1px,transparent_1px)] [background-size:16px_16px]"></div>
         <!-- Dashboard Grid -->
         <div class="relative z-10 grid grid-cols-2 gap-3 h-full">
            <!-- CPU -->
            <div class="bg-[#131418] border border-[#2e3036] rounded p-2">
               <div class="flex justify-between items-center mb-2">
                  <span class="text-[10px] text-gray-400">CPU Usage</span>
                  <span class="text-[10px] text-gray-500">...</span>
               </div>
               <div class="h-12 flex items-end gap-0.5">
                  {#each Array(20) as _, i}
                    <div class="w-full bg-purple-500/40" style="height: {Math.random() * 100}%"></div>
                  {/each}
               </div>
            </div>
            <!-- Memory -->
            <div class="bg-[#131418] border border-[#2e3036] rounded p-2">
               <div class="flex justify-between items-center mb-2">
                  <span class="text-[10px] text-gray-400">Memory Usage</span>
                  <span class="text-[10px] text-gray-500">...</span>
               </div>
               <div class="h-12 flex items-end gap-0.5">
                  {#each Array(20) as _, i}
                    <div class="w-full bg-blue-500/40" style="height: {Math.random() * 80}%"></div>
                  {/each}
               </div>
            </div>
            <!-- Errors -->
            <div class="bg-[#131418] border border-[#2e3036] rounded p-2">
               <div class="flex justify-between items-center mb-2">
                  <span class="text-[10px] text-gray-400">5XX Errors</span>
                  <span class="text-[10px] text-gray-500">...</span>
               </div>
               <div class="h-12 flex items-end gap-0.5">
                  {#each Array(20) as _, i}
                    <div class="w-full bg-red-500/40" style="height: {Math.random() * 20}%"></div>
                  {/each}
               </div>
            </div>
            <!-- Network -->
            <div class="bg-[#131418] border border-[#2e3036] rounded p-2">
               <div class="flex justify-between items-center mb-2">
                  <span class="text-[10px] text-gray-400">Network Egress</span>
                  <span class="text-[10px] text-gray-500">...</span>
               </div>
               <div class="h-12 flex items-end gap-0.5">
                  {#each Array(20) as _, i}
                    <div class="w-full bg-green-500/40" style="height: {Math.random() * 60}%"></div>
                  {/each}
               </div>
            </div>
         </div>
      </div>
    </Feature>

    <!-- Feature 5: Evolve and Collaborate -->
    <Feature 
      title="Evolve and Collaborate"
      headline="Accelerate development with PR environments, baremetal builds, and automatic infrastructure versioning"
      description="Seamlessly evolve your infrastructure with forking, automatic versioning, and team roles for faster-than-cloud build times."
      color="green"
      align="left"
    >
      <div slot="stats" class="flex items-center gap-2 text-sm text-gray-400 mb-6">
         <svg class="w-5 h-5 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" /></svg>
         <span class="text-white font-bold">50%</span> faster builds
      </div>
      <div slot="visual" class="w-full h-full min-h-[400px] bg-[#0b0c0e] p-6 relative flex flex-col gap-6 justify-center">
         <div class="absolute inset-0 bg-[radial-gradient(#1c1d22_1px,transparent_1px)] [background-size:16px_16px]"></div>
         
         <div class="relative z-10 grid grid-cols-2 gap-6">
             <!-- Production Environment -->
             <div class="bg-[#131418] border border-[#2e3036] rounded-lg p-4 relative">
                <div class="flex items-center gap-2 mb-4">
                    <svg class="w-4 h-4 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" /></svg>
                    <span class="text-sm font-medium text-white">production</span>
                </div>
                <div class="space-y-2">
                    <div class="h-8 bg-[#0b0c0e] border border-[#2e3036] rounded flex items-center px-2 gap-2">
                        <div class="w-2 h-2 bg-green-500 rounded-full"></div>
                        <div class="h-1 w-12 bg-gray-700 rounded"></div>
                    </div>
                    <div class="h-8 bg-[#0b0c0e] border border-[#2e3036] rounded flex items-center px-2 gap-2">
                        <div class="w-2 h-2 bg-green-500 rounded-full"></div>
                        <div class="h-1 w-16 bg-gray-700 rounded"></div>
                    </div>
                </div>
                <!-- User Avatar -->
                <div class="absolute -top-3 -right-3 w-8 h-8 rounded-full bg-gray-700 border-2 border-[#131418] flex items-center justify-center text-[10px]">JD</div>
             </div>

             <!-- Development Environment -->
             <div class="bg-[#131418] border border-[#2e3036] rounded-lg p-4 relative opacity-80">
                <div class="flex items-center gap-2 mb-4">
                    <svg class="w-4 h-4 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" /></svg>
                    <span class="text-sm font-medium text-white">development</span>
                </div>
                <div class="space-y-2">
                    <div class="h-8 bg-[#0b0c0e] border border-[#2e3036] rounded flex items-center px-2 gap-2">
                        <div class="w-2 h-2 bg-blue-500 rounded-full"></div>
                        <div class="h-1 w-10 bg-gray-700 rounded"></div>
                    </div>
                    <div class="h-8 bg-[#0b0c0e] border border-[#2e3036] rounded flex items-center px-2 gap-2">
                        <div class="w-2 h-2 bg-blue-500 rounded-full"></div>
                        <div class="h-1 w-14 bg-gray-700 rounded"></div>
                    </div>
                </div>
                <!-- User Avatar -->
                <div class="absolute -top-3 -right-3 w-8 h-8 rounded-full bg-gray-700 border-2 border-[#131418] flex items-center justify-center text-[10px]">AB</div>
             </div>
         </div>
      </div>
    </Feature>

    <Testimonials />
    <Community />
    <Stats />
  </main>

  <Footer />
</div>

