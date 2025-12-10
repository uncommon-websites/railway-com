<script>
  const logos = [
    { name: 'Tripadvisor', width: 100 },
    { name: 'G2X', width: 40 },
    { name: 'Apollo', width: 80 },
    { name: 'Clerk', width: 60 },
    { name: 'Prisma', width: 70 },
    { name: 'Arcol', width: 50 },
    { name: 'Chatbase', width: 80 },
    { name: 'Kaishi', width: 60 },
    { name: 'Intuit', width: 60 },
    { name: 'Peerlist', width: 70 },
    { name: 'RE/MAX', width: 80 },
    { name: 'TEKTON', width: 80 },
    { name: 'Profound', width: 80 },
    { name: 'Sleek', width: 50 },
    { name: 'Zillow', width: 60 },
    { name: 'MGM RESORTS', width: 100 },
    { name: 'EVERY', width: 60 }
  ];
</script>

<section class="border-b border-[#2e3036] bg-[#0b0c0e] py-8 overflow-hidden">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex flex-wrap justify-center items-center gap-x-8 gap-y-6 opacity-40 grayscale">
      <!-- I will use text for logos as placeholders for the real SVGs to keep it clean and fast -->
      {#each logos as logo}
        <div class="text-lg font-bold text-gray-400 select-none">{logo.name}</div>
      {/each}
    </div>
  </div>
</section>
