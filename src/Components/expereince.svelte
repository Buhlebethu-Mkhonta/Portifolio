<script>
  let items = [
    {
      title: "IT Middle Manager",
      company: "The Luke Commission, Eswatini",
      period: "2023 - 2025",
      details: [
        "Piloted drones for Eswatini's first medical drone network, contributing to innovative healthcare delivery",
        "Installed and configured UNIFI network equipment across organizational sites, maintaining robust wireless networks.",
        "Developed and maintained IT documentation for system configurations and troubleshooting procedures.",
        "Authored SOPs and internal documentation for IT infrastructure and drone operations.",
        "Maintained inventory tracking for over 100+ devices, including laptops, desktops, and mobile hardware.",
        "Collaborated across departments to deliver IT solutions aligned with user needs."

      ]
    },
    {
      title: "Web developer Intern",
      company: "Onswaziline Investments, Eswatini",
      period: "2021 - 2021",
      details: [
        "Updated and maintained client websites, including frontend improvements and content updates.",
        "Communicated directly with clients (e.g., Eswatini Electrical Company, Ekupholeni Garden Villas) to gather requirements and deliver website modifications",
        "Shadowed senior developers to enhance web development and client management skills.",
        
      ]
    },
    // Add more items as needed
  ];
</script>

<section id="experience" class=" bg-[#181c23] py-12 px-2 sm:px-4">
    <div class="text-center mb-12">
        <span class="inline-block bg-[#23272f] text-white text-sm px-4 py-1 rounded-full mb-2">Professional Journey</span>
        <h2 class="text-4xl md:text-5xl font-extrabold text-white mb-2">
          Work Experience
        </h2>
        <div class="w-24 h-1 bg-red-500 mx-auto rounded"></div>
    </div>
  <div class="flex flex-col items-center gap-8 max-w-3xl mx-auto w-full">
    {#each items as item}
      <div class="card w-full bg-[#23272f] shadow-xl border border-[#23272f]">
        <div class="card-body p-5 sm:p-8">
          <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between mb-2 gap-2">
            <h3 class="card-title text-lg sm:text-xl text-white font-semibold">{item.title}</h3>
            <span class="badge bg-[#ff2d2d] text-white text-sm font-bold px-4 py-2 rounded-full shadow border-none">{item.period}</span>
          </div>
          <div class="text-[#b0b8c1] mb-2 font-medium">{item.company}</div>
          <ul class="list-disc list-inside space-y-1">
            {#each item.details as detail}
              <li class="text-[#d1d5db] text-base leading-relaxed">{detail}</li>
            {/each}
          </ul>
        </div>
      </div>
    {/each}
  </div>
</section>
