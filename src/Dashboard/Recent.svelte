<script>
  // مصفوفة لتخزين النماذج الحديثة
  let recentForms = [];

  // دالة لإضافة نموذج جديد
  function addNewForm() {
    const newForm = {
      id: Date.now(), // معرف فريد
      title: "New Form",
      subtitle: "Just added"
    };
    recentForms = [newForm, ...recentForms]; // إضافة النموذج على رأس القائمة
  }
</script>

<!-- زر إنشاء نموذج جديد -->
<div class="flex justify-start py-4">
  <button 
    on:click={addNewForm} 
    class="group flex flex-col items-center justify-center w-48 h-60
           bg-gradient-to-br from-[#50B498] to-[#468585]
           text-white text-xl font-bold rounded-xl shadow-lg
           hover:shadow-xl hover:scale-[1.03] transition-all duration-200
           select-none"
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

<!-- قسم Recent Forms -->
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
