<script>
  const tweets = [
    { name: 'Moretti', handle: '@moretti_dev', text: 'Railway streamlines and accelerates our operation. It gives us instant observability into our services and makes spinning up self-hosted third-party tools almost effortless.' },
    { name: 'Pingback Inc', handle: '@pingbackofficial', text: 'As CTO at Pingback, speed of iteration is everything for us. @Railway has become our go-to platform for rapid experimentation and testing new ideas.' },
    { name: 'Aaron S', handle: '@aaron_s', text: 'Typically, I avoid using PaaS but the team at @Railway is boosting development velocity so significantly that it\'s hard to ignore' },
    { name: 'John Nunemaker', handle: '@jnunemaker', text: 'I\'ve moved $4.5k/mo worth of infrastructure from Heroku in the past week. The DX on @Railway bill is like 1/3.' },
    { name: 'Teo', handle: '@teo_io', text: '@Railway is really really good. Being able to deploy straight from a Github repo, detecting a root Dockerfile and using that to build, no need for any complex cicd, will re-deploy for every push.' },
    { name: 'Brandon Geli', handle: '@brandongeli', text: 'We 🚂 are 🚂 on 🚂 Railway 🚂. $1600 on Heroku -> $300 on @Railway.' },
    { name: 'Mohit', handle: '@mohit', text: '@Railway is kinda magic. I just pick a template (like Umami or Uptime Kuma), hit deploy, and boom - it\'s live.' }
  ];
</script>

<section class="py-24 border-t border-[#2e3036] overflow-hidden">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center mb-16">
      <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">...and loved by developers</h2>
      <a href="#" class="text-gray-400 hover:text-white text-sm font-medium inline-flex items-center">
        Join nearly 2M developers building with Railway <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" /></svg>
      </a>
    </div>

    <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
      {#each tweets as tweet}
        <div class="break-inside-avoid bg-[#131418] border border-[#2e3036] p-6 rounded-xl hover:border-gray-600 transition-colors">
          <div class="flex items-center gap-3 mb-4">
             <div class="w-10 h-10 rounded-full bg-gray-700"></div>
             <div>
                <div class="text-white font-bold text-sm">{tweet.name}</div>
                <div class="text-gray-500 text-xs">{tweet.handle}</div>
             </div>
             <svg class="w-4 h-4 text-gray-600 ml-auto" fill="currentColor" viewBox="0 0 24 24"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/></svg>
          </div>
          <p class="text-gray-300 text-sm leading-relaxed">
            {tweet.text}
          </p>
        </div>
      {/each}
    </div>
  </div>
</section>
