<script>
  // مصفوفة لتخزين النماذج الحديثة
  let recentForms = [];

  // دالة لإضافة نموذج جديد
  function onAddNew() {
    const newForm = {
      id: Date.now(),   // معرف فريد
      title: "New Form",
      subtitle: "Just added"
    };
    recentForms = [newForm, ...recentForms]; // نضيف النموذج للأعلى
  }
</script>

<!-- ░░░ HERO SECTION ░░░ -->
<section class="bg-gray-100 text-gray-900 w-full min-h-screen">
  <div class="max-w-5xl mx-auto pt-10 px-4">

    <!-- Header Row -->
    <div class="flex justify-between items-center mb-6 select-none">
      <span class="text-xl font-semibold text-[#468585] tracking-wide">Start a new document</span>

      <button class="flex items-center gap-1 text-gray-700 hover:text-[#50B498] transition font-medium" aria-label="Template gallery">
        <span>Template gallery</span>
        <svg xmlns="http://www.w3.org/2000/svg" 
             class="w-4 h-4" fill="none" viewBox="0 0 24 24" 
             stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M19 9l-7 7-7-7" />
        </svg>
      </button>
    </div>

    <!-- New Form Card -->
    <div class="flex justify-start py-4">
      <button 
        on:click={onAddNew}
        class="group flex flex-col items-center justify-center w-48 h-60
               bg-gradient-to-br from-[#50B498] to-[#468585]
               text-white text-xl font-bold rounded-xl shadow-lg
               hover:shadow-xl hover:scale-[1.03] transition-all duration-200
               select-none"
        aria-label="Add new form"
        title="Create a new form"
      >
        <div class="bg-white/20 rounded-full p-6 mb-3 group-hover:bg-white/30 transition">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-14 h-14" fill="none" viewBox="0 0 24 24" 
               stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M12 4v16m8-8H4" />
          </svg>
        </div>

        <span class="tracking-wide">New Form</span>
      </button>
    </div>

    <!-- Extra visual separation -->
    <div class="border-t border-gray-300/40 my-10"></div>

    <!-- Optional subtitle for next section -->
    <p class="text-gray-600 text-md px-1 select-none">
      Recently opened forms will appear below.
    </p>

    <!-- Recent Forms Section -->
    <div class="mt-6 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
      {#if recentForms.length === 0}
        <!-- Placeholder إذا لم توجد نماذج -->
        <div class="flex flex-col items-center justify-center h-40 bg-white/50 border-2 border-dashed border-gray-400 rounded-xl text-gray-500 select-none">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 mb-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path d="M12 4v16m8-8H4" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          <span>Empty</span>
          <small class="text-xs text-gray-400">No form yet</small>
        </div>
      {:else}
        {#each recentForms as form}
          <!-- بطاقة النموذج -->
          <div class="flex flex-col items-center justify-center h-40 bg-white border rounded-xl shadow-sm hover:shadow-md transition select-none">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 mb-2 text-[#50B498]" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path d="M12 4v16m8-8H4" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <span class="font-medium">{form.title}</span>
            <small class="text-xs text-gray-400">{form.subtitle}</small>
          </div>
        {/each}
      {/if}
    </div>

  </div>
</section>
