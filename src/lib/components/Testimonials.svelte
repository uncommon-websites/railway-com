<script>
  const testimonials = [
    {
      company: 'BILT',
      quote: "On our previous rent day, we saw traffic of 1,500+ requests per second that were all being fulfilled in under 50 milliseconds, which is really great. Our technical team is really impressed with scale like that.",
      author: 'Kartik Aggarwal',
      role: 'Tech Lead at Bilt',
      logo: 'B'
    },
    {
      company: 'G2X',
      quote: "Services that took 1 week to configure elsewhere take 1 day to spin up in Railway. Messy networking like on other cloud platforms doesn't exist on Railway. If you understand basic TCP, you're all set.",
      author: 'Daniel Lobaton',
      role: 'CTO at G2X',
      logo: 'G'
    },
    {
      company: 'Mappa',
      quote: "Railway streamlines and accelerates our entire operation. It gives us instant observability into our services and makes spinning up self-hosted third-party tools almost effortless. This reduces friction in experimentation and shortens our deployment cycles significantly.",
      author: 'Daniel Moretti',
      role: 'Co-Founder & CTO at Mappa',
      logo: 'M'
    },
    {
      company: 'Capitalize',
      quote: "Railway has been a revelation. We spent ~$100K per year running on AWS - we have since cut that by 90% moving to Railway and get a significantly improved developer experience. I wish I had this years ago.",
      author: 'Antoine Vulcain',
      role: 'Founder & CEO at Capitalize',
      logo: 'C'
    }
  ];
</script>

<section class="py-32 border-t border-[#2e3036]">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-20">
      <h2 class="text-3xl md:text-5xl font-bold text-white mb-6">Trusted by the best in business</h2>
      <p class="text-xl text-gray-400 mb-8">
        Railway supports great software teams wherever they are. Hear from some of the teams building their products on Railway.
      </p>
      <a href="#" class="text-gray-400 hover:text-white text-sm font-medium inline-flex items-center">
        Read customer stories <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" /></svg>
      </a>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      {#each testimonials as t}
        <div class="bg-[#131418] border border-[#2e3036] p-8 rounded-xl hover:border-gray-600 transition-colors">
          <div class="flex items-center gap-2 mb-6">
             <div class="w-8 h-8 rounded bg-gray-800 flex items-center justify-center font-bold text-white">{t.logo}</div>
             <span class="font-bold text-white">{t.company}</span>
          </div>
          <p class="text-gray-300 mb-8 leading-relaxed">"{t.quote}"</p>
          <div class="flex items-center gap-3">
             <div class="w-10 h-10 rounded-full bg-gray-700"></div>
             <div>
                <div class="text-white font-medium text-sm">{t.author}</div>
                <div class="text-gray-500 text-xs">{t.role}</div>
             </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
