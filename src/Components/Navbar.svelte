<script>
  import { onMount } from 'svelte';
  import { Lucide } from '@lucide/astro';
  import { fly } from 'svelte/transition';

  let currentSection = '';

  function scrollToSection(event, sectionId) {
    event.preventDefault();
    const element = document.getElementById(sectionId);
    if (element) {
      currentSection = sectionId;
      const targetPosition = element.getBoundingClientRect().top + window.pageYOffset;
      const startPosition = window.pageYOffset;
      const distance = targetPosition - startPosition;
      const duration = 2000; // 2 seconds
      let start = null;

      function animation(currentTime) {
        if (start === null) start = currentTime;
        const timeElapsed = currentTime - start;
        const progress = Math.min(timeElapsed / duration, 1);
        
        // Using Svelte's fly transition easing
        const easeOutCubic = t => 1 - Math.pow(1 - t, 3);
        
        window.scrollTo(0, startPosition + distance * easeOutCubic(progress));

        if (timeElapsed < duration) {
          requestAnimationFrame(animation);
        }
      }

      requestAnimationFrame(animation);
    }
  }
</script>

<div class="navbar shadow-sm bg-[#181c23]  top-0 left-0 right-0 z-50">
  <div class="navbar-start">
    <div class="dropdown ">
      <div tabindex="0" role="button" class="btn btn-ghost lg:hidden text-white hover:bg-transparent">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"> <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" /> </svg>
      </div>
      <ul
        class="menu menu-sm dropdown-content bg-base-100 rounded-box z-1 mt-3 w-52 p-2 shadow text-black "
        in:fly={{ y: -20, duration: 300, delay: 0 }}>
        <li><a href="#about" on:click={(e) => scrollToSection(e, 'about')} class:active={currentSection === 'about'}>About</a></li>
        <li><a href="#skills" on:click={(e) => scrollToSection(e, 'skills')} class:active={currentSection === 'skills'}>Skills</a></li>
        <li><a href="#experience" on:click={(e) => scrollToSection(e, 'experience')} class:active={currentSection === 'experience'}>Experience</a></li>
        <li><a href="#certifications" on:click={(e) => scrollToSection(e, 'certifications')} class:active={currentSection === 'certifications'}>Certifications</a></li>
        <li><a href="#projects" on:click={(e) => scrollToSection(e, 'projects')} class:active={currentSection === 'projects'}>Projects</a></li>
        <li><a href="#contact" on:click={(e) => scrollToSection(e, 'contact')} class:active={currentSection === 'contact'}>Contact</a></li>
      </ul>
    </div>
    <span class="text-2xl font-bold text-white tracking-wide">BM<span class="text-red-500">.</span></span>
  </div>
  <div class="navbar-center hidden lg:flex">
    <ul class="menu menu-horizontal px-1 text-white">
      <li class="hover:text-red-500 transition"><a href="#about" on:click={(e) => scrollToSection(e, 'about')} class:active={currentSection === 'about'}>About</a></li>
      <li class="hover:text-red-500 transition"><a href="#skills" on:click={(e) => scrollToSection(e, 'skills')} class:active={currentSection === 'skills'}>Skills</a></li>
      <li class="hover:text-red-500 transition"><a href="#experience" on:click={(e) => scrollToSection(e, 'experience')} class:active={currentSection === 'experience'}>Experience</a></li>
      <li class="hover:text-red-500 transition"><a href="#certifications" on:click={(e) => scrollToSection(e, 'certifications')} class:active={currentSection === 'certifications'}>Certifications</a></li>
      <li class="hover:text-red-500 transition"><a href="#projects" on:click={(e) => scrollToSection(e, 'projects')} class:active={currentSection === 'projects'}>Projects</a></li>
      <li class="hover:text-red-500 transition"><a href="#contact" on:click={(e) => scrollToSection(e, 'contact')} class:active={currentSection === 'contact'}>Contact</a></li>
    </ul>
  </div>
  <div class="navbar-end px-5">
    <a href="#contact" class="btn bg-red-500 rounded-4xl text-white border-none" on:click={(e) => scrollToSection(e, 'contact')}>Lets Work Together</a>
  </div>
</div>

<style>
  :global(.active) {
    color: #ef4444 !important; /* text-red-500 */
  }
</style>

