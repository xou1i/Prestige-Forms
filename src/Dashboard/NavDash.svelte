<script>
  function handleMyFormsClick() {
    alert("You clicked on My Forms!");
    // يمكنك هنا إضافة أي منطق إضافي
  }
</script>

<nav class="bg-white/70 backdrop-blur-md p-4 sticky top-0 z-50 shadow-sm border-b border-gray-300/40">
  <div class="max-w-5xl mx-auto flex justify-between items-center">
    
    <!-- Logo -->
    <h1 class="text-3xl font-bold tracking-tight text-gray-900 select-none">
      Form<span class="text-[#50B498]">Hub</span>
    </h1>

    <!-- Right button -->
    <button on:click={handleMyFormsClick} class="px-4 py-2 rounded-lg bg-[#50B498] hover:bg-[#3f8c75] text-white font-semibold transition">
      My Forms
    </button>
  </div>
</nav>
