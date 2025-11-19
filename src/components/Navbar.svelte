<script>
  let menuOpen = false;
  let closing = false;

  function toggleMenu() {
    if (menuOpen) {
      closing = true;
      setTimeout(() => {
        menuOpen = false;
        closing = false;
      }, 300);
    } else {
      menuOpen = true;
    }
  }
</script>

<nav class="fixed top-0 left-0 w-full z-50
            bg-white/30 backdrop-blur-2xl
            border-b border-white/60
            shadow-[0_8px_32px_rgba(0,0,0,0.05)]">

  <div class="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between">

    <!-- Logo -->
    <div 
      class="text-3xl font-bold tracking-wider cursor-pointer text-[#FFB74D]"
      style="font-family: 'Sooner', sans-serif;"
    >
      Prestige
    </div>

    <!-- Desktop Links -->
    <ul class="hidden md:flex items-center space-x-4">
      <li><a href="#home"
        class="px-4 py-2 rounded-full border-2 border-[#011E6C] text-[#011E6C]
               hover:bg-[#011E6C] hover:text-white transition-all">Home</a></li>

      <li><a href="#about"
        class="px-4 py-2 rounded-full border-2 border-[#011E6C] text-[#011E6C]
               hover:bg-[#011E6C] hover:text-white transition-all">About</a></li>

      <li><a href="#skills"
        class="px-4 py-2 rounded-full border-2 border-[#011E6C] text-[#011E6C]
               hover:bg-[#011E6C] hover:text-white transition-all">Skills</a></li>

      <li><a href="#projects"
        class="px-4 py-2 rounded-full border-2 border-[#011E6C] text-[#011E6C]
               hover:bg-[#011E6C] hover:text-white transition-all">Projects</a></li>

               <li><a href="#Experience"
        class="px-4 py-2 rounded-full border-2 border-[#011E6C] text-[#011E6C]
               hover:bg-[#011E6C] hover:text-white transition-all">Experience</a></li>

      <li><a href="#contact"
        class="px-4 py-2 rounded-full border-2 border-[#011E6C] text-[#011E6C]
               hover:bg-[#011E6C] hover:text-white transition-all">Contact</a></li>
    </ul>

    <!-- Mobile Menu Button -->
    <button
      class="md:hidden p-3 rounded-lg text-[#011E6C] hover:text-[#1A3FA3] transition"
      on:click={toggleMenu}
    >
      {#if !menuOpen}
        <!-- Hamburger Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none"
             viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round"
                d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      {:else}
        <!-- Close Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none"
             viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12" />
        </svg>
      {/if}
    </button>
  </div>
</nav>

<!-- Mobile Menu -->
{#if menuOpen || closing}
  <div 
  class="md:hidden fixed top-16 left-0 w-full
         bg-white/30 backdrop-blur-2xl
         shadow-lg border-b border-white/40
         p-6 space-y-4 z-40"
  class:animate-menuOpen={menuOpen}
  class:animate-menuClose={closing}
>


    <a href="#home"
      class="block text-lg text-[#011E6C]
             px-4 py-2 rounded-full border border-[#011E6C]
             hover:bg-[#011E6C] hover:text-white transition-all">Home</a>

    <a href="#about"
      class="block text-lg text-[#011E6C]
             px-4 py-2 rounded-full border border-[#011E6C]
             hover:bg-[#011E6C] hover:text-white transition-all">About</a>

    <a href="#skills"
      class="block text-lg text-[#011E6C]
             px-4 py-2 rounded-full border border-[#011E6C]
             hover:bg-[#011E6C] hover:text-white transition-all">Skills</a>

    <a href="#projects"
      class="block text-lg text-[#011E6C]
             px-4 py-2 rounded-full border border-[#011E6C]
             hover:bg-[#011E6C] hover:text-white transition-all">Projects</a>

             <a href="#Experience"
      class="block text-lg text-[#011E6C]
             px-4 py-2 rounded-full border border-[#011E6C]
             hover:bg-[#011E6C] hover:text-white transition-all">Experience</a>

    <a href="#contact"
      class="block text-lg text-[#011E6C]
             px-4 py-2 rounded-full border border-[#011E6C]
             hover:bg-[#011E6C] hover:text-white transition-all">Contact</a>
  </div>
{/if}

<style>
  @keyframes menuOpen {
    0%   { opacity: 0; transform: translateY(-20px); }
    100% { opacity: 1; transform: translateY(0); }
  }

  @keyframes menuClose {
    0%   { opacity: 1; transform: translateY(0); }
    100% { opacity: 0; transform: translateY(-20px); }
  }

  .animate-menuOpen {
    animation: menuOpen 0.3s ease-out forwards;
  }

  .animate-menuClose {
    animation: menuClose 0.3s ease-in forwards;
  }

</style>
