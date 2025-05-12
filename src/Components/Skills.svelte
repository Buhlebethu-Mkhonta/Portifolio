<script>
    import {onMount} from 'svelte';
</script>

<section id="skills" class="py-16 bg-white">
  <div class="max-w-6xl mx-auto px-4">
    <div class="text-center mb-12">
      <span class="inline-block bg-gray-200 text-gray-700 text-sm px-4 py-1 rounded-full mb-2">My Expertise</span>
      <h2 class="text-4xl md:text-5xl font-extrabold text-gray-900 mb-2">
        Professional Skills
      </h2>
      <div class="w-24 h-1 bg-red-500 mx-auto rounded"></div>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <!-- Drone Operations -->
      <div class="bg-gray-50 rounded-2xl shadow transition-shadow duration-300 hover:shadow-xl/30 p-8 flex flex-col">
        <i class='bx bxs-plane-alt text-4xl text-red-500 mb-5' ></i>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Drone Operations</h3>
        <p class="text-gray-700 mb-4">
          Expert in BVLOS drone piloting for medical logistics, aerial surveys, and specialized operations in challenging environments.
        </p>
        <div class="flex flex-wrap gap-2">
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Medical Logistics</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">BVLOS Operations</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Flight Planning</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Aerial Mapping</span>
        </div>
      </div>
      <!-- IT Infrastructure -->
      <div class="bg-gray-50 rounded-2xl shadow transition-shadow duration-300 hover:shadow-xl/30 p-8 flex flex-col">
        <i class='bx bx-sitemap text-4xl text-red-500 mb-5' ></i>
        <h3 class="text-xl font-bold text-gray-900 mb-2">IT Infrastructure</h3>
        <p class="text-gray-700 mb-4">
          Specialized in deploying and managing robust IT networks, server administration, and UNIFI systems implementation.
        </p>
        <div class="flex flex-wrap gap-2">
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">UNIFI Networks</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Server Management</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Technical Support</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Troubleshooting</span>
        </div>
      </div>
      <!-- Web Development -->
      <div class="bg-gray-50 rounded-2xl shadow transition-shadow duration-300 hover:shadow-xl/30 p-8 flex flex-col">
        <i class='bx bx-code-alt text-4xl text-red-500 mb-5' ></i>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Web Development</h3>
        <p class="text-gray-700 mb-4">
          Creating and maintaining responsive websites with focus on user experience, performance, and modern design principles.
        </p>
        <div class="flex flex-wrap gap-2">
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">HTML/CSS</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">JavaScript</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Responsive Design</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">CMS</span>
        </div>
      </div>
      <!-- Technical Support -->
      <div class="bg-gray-50 rounded-2xl shadow transition-shadow duration-300 hover:shadow-xl/30 p-8 flex flex-col">
        <i class='bx bx-support text-4xl text-red-500 mb-5' ></i>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Technical Support</h3>
        <p class="text-gray-700 mb-4">
          Providing comprehensive hardware and software troubleshooting, with excellent documentation and customer service skills.
        </p>
        <div class="flex flex-wrap gap-2">
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Hardware Diagnostics</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Software Support</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Documentation</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Customer Service</span>
        </div>
      </div>
      <!-- Emerging Technologies -->
      <div class="bg-gray-50 rounded-2xl shadow transition-shadow duration-300 hover:shadow-xl/30] p-8 flex flex-col">
        <i class='bx bxs-chip text-4xl text-red-500 mb-5' ></i>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Emerging Technologies</h3>
        <p class="text-gray-700 mb-4">
          Exploring and implementing AI, automation, and cutting-edge tech solutions for business and operational challenges.
        </p>
        <div class="flex flex-wrap gap-2">
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Artificial Intelligence</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Automation</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">IoT</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Tech Research</span>
        </div>
      </div>
      <!-- Technical Documentation -->
      <div class="bg-gray-50 rounded-2xl shadow transition-shadow duration-300 hover:shadow-xl/30 p-8 flex flex-col">
        <i class='bx bxs-file text-4xl text-red-500 mb-5' ></i>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Technical Documentation</h3>
        <p class="text-gray-700 mb-4">
          Creating clear, comprehensive documentation for systems, processes, and technical implementations.
        </p>
        <div class="flex flex-wrap gap-2">
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Process Mapping</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Technical Writing</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">Knowledge Bases</span>
          <span class="bg-gray-200 text-gray-700 text-xs px-3 py-1 rounded-full">User Guides</span>
        </div>
      </div>
    </div>
  </div>
</section>
