<script>
  // Home components
  import Nav from "./Home/Nav.svelte"
  import Hero from "./Home/Hero.svelte"

  // login components
  import NavLogin from "./Login/NavLogin.svelte";
  import HeroLogin from "./Login/HeroLogin.svelte";

// Dashboard components
  import NavDash from "./Dashboard/NavDash.svelte";
  import HeroDash from "./Dashboard/HeroDash.svelte";

  // Create component
  import NavCreate from "./Create/NavCreate.svelte";
  import HeroCreate from "./Create/HeroCreate.svelte";
</script>


<Nav />
<Hero />

<NavLogin />
<HeroLogin />

<NavDash />
<HeroDash />

<NavCreate />
<HeroCreate />



<main class="p-10"></main>
