<script>
    export let title = "Design forms people enjoy using";
    export let subtitle =
        "Create beautiful, accessible forms with drag & drop, instant publishing, and analytics built-in.";
    export let cta = "Get started — it’s free";
    export let ctaHref = "#get-started";
</script>

<section class="bg-white dark:bg-slate-900">
    <div class="max-w-7xl mx-auto px-6 lg:px-8 py-16 lg:py-24">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div>
                <h1
                    class="text-3xl sm:text-4xl font-extrabold text-slate-900 dark:text-white tracking-tight"
                >
                    {title}
                </h1>
                <p
                    class="mt-4 text-lg text-slate-600 dark:text-slate-300 max-w-xl"
                >
                    {subtitle}
                </p>

                <div
                    class="mt-8 flex flex-col sm:flex-row sm:items-center sm:space-x-4 space-y-3 sm:space-y-0"
                >
                    <a
                        href={ctaHref}
                        class="inline-flex items-center justify-center rounded-md bg-indigo-600 hover:bg-indigo-700 px-6 py-3 text-white font-medium shadow"
                        >{cta}</a
                    >
                    <a
                        href="#learn-more"
                        class="inline-flex items-center justify-center rounded-md border border-slate-200 dark:border-slate-700 px-6 py-3 text-slate-700 dark:text-slate-200 hover:bg-slate-50 dark:hover:bg-slate-800"
                        >Learn more</a
                    >
                </div>

                <ul
                    class="mt-8 flex flex-wrap gap-3 text-sm text-slate-500 dark:text-slate-300"
                >
                    <li
                        class="inline-flex items-center gap-2 bg-slate-50 dark:bg-slate-800 px-3 py-1 rounded-full"
                    >
                        ⚡ Fast setup
                    </li>
                    <li
                        class="inline-flex items-center gap-2 bg-slate-50 dark:bg-slate-800 px-3 py-1 rounded-full"
                    >
                        🎨 Custom themes
                    </li>
                    <li
                        class="inline-flex items-center gap-2 bg-slate-50 dark:bg-slate-800 px-3 py-1 rounded-full"
                    >
                        📊 Built‑in analytics
                    </li>
                </ul>
            </div>

            <div class="flex items-center justify-center">
                <div
                    class="w-full max-w-md rounded-2xl overflow-hidden shadow-lg ring-1 ring-slate-900/5 dark:ring-white/5"
                >
                    <img
                        src="/PRESTIGE.png"
                        alt="Prestige preview"
                        class="w-full h-auto object-cover bg-slate-100 dark:bg-slate-800"
                    />
                </div>
            </div>
        </div>
    </div>
</section>
