<script>
    import { onMount } from 'svelte';

    
</script>

<div id="about" class="flex flex-col md:flex-row items-center justify-center min-h-screen bg-gray-50 px-4 py-12">
  <!-- Profile Image -->
  <div class="flex-shrink-0 mb-8 md:mb-0 md:mr-12">
    <img
      src="/images/Profile.png"
      alt="Buhlebethu Mkhonta profile"
      class="rounded-2xl shadow-xl/30 w-100 h-120 object-cover "
    />
  </div>
  <!-- About Content -->
  <div class="max-w-2xl w-full">
    <span class="inline-block bg-gray-200 text-gray-700 text-sm px-4 py-1 rounded-full mb-4">About Me</span>
    <h1 class="text-4xl md:text-5xl font-extrabold text-gray-900 mb-4">Buhlebethu Mkhonta</h1>
    <p class="text-gray-700 text-lg mb-4">
      I'm a multifaceted tech professional with expertise in drone operations and IT infrastructure. As one of the pioneers behind Eswatini's first medical drone network, I've combined my passion for aerial technology with practical applications that save lives.
    </p>
    <p class="text-gray-700 text-lg mb-6">
      Currently pursuing my Masters in AI, I'm constantly exploring the intersection of emerging technologies. When I'm not troubleshooting networks or piloting drones, you might find me skateboarding or enjoying rock and metal music – activities that inspire my creative approach to technical challenges.
    </p>
    <!-- Roles -->
    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
      <div class="flex flex-col items-center bg-white rounded-xl shadow p-4">
        <span class="text-red-500 text-4xl mb-2"><i class='bx bxs-plane-alt'></i></span>
        <span class="font-semibold text-gray-900">Drone Pilot</span>
      </div>
      <div class="flex flex-col items-center bg-white rounded-xl shadow p-4">
        <span class="text-red-500 text-4xl mb-2"><i class='bx bx-sitemap'></i></span>
        <span class="font-semibold text-gray-900">IT Specialist</span>
      </div>
      <div class="flex flex-col items-center bg-white rounded-xl shadow p-4">
        <span class="text-red-500 text-4xl mb-2"><i class='bx bx-code-alt'></i></span>
        <span class="font-semibold text-gray-900">Web Developer</span>
      </div>
      <div class="flex flex-col items-center bg-white rounded-xl shadow p-4">
        <span class="text-red-500 text-4xl mb-2"><i class='bx bxs-bot'></i></span>
        <span class="font-semibold text-gray-900">AI Enthusiast</span>
      </div>
    </div>
    <!-- Buttons -->
    <div class="flex flex-col sm:flex-row gap-4">
    
      
      <!--
      <button class="flex items-center justify-center gap-2 border border-gray-900 text-gray-900 text-lg px-8 py-3 rounded-full font-semibold bg-white hover:bg-gray-900 hover:text-white transition">
        <i class='bx bxs-folder-open'></i>
        <span>View Portfolio</span>
      </button>
    -->
    </div>
  </div>
</div>
