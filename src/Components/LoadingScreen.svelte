<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';

  let loading = true;

  onMount(() => {
    // Check if this is the first load
    const hasLoaded = sessionStorage.getItem('hasLoaded');
    
    if (hasLoaded) {
      loading = false;
      return;
    }

    setTimeout(() => {
      loading = false;
      sessionStorage.setItem('hasLoaded', 'true');
    }, 3000); // Show for 3 seconds
  });
</script>

{#if loading}
  <div 
    class="fixed inset-0 bg-[#181c23] z-50 flex items-center justify-center"
    transition:fade={{ duration: 400 }}
  >
    <div class="text-center">
      <!-- Pulsing BM Logo -->
      <div class="relative w-32 h-32">
        <div class="absolute inset-0 flex items-center justify-center">
          <div class="text-6xl font-bold tracking-wider animate-pulse-text">
            <span class="inline-block">BM</span>
            
          </div>
        </div>
      </div>
    </div>
  </div>
{/if}

<style>
 
</style> 