<script>
	import router from 'page';
  import Sidenav from './components/Sidenav.svelte';
  import Navbar from './components/Navbar.svelte';
  import Dashboard from './area/Dashboard/Page.svelte'

  let page;
  let params;

  router('/Dashboard', () => page = Dashboard);

  router.start();
</script>

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="http://ordermygear.com">
      Property Management
    </a>
  </div>
</nav>

<main class="page">
  <Sidenav />
  <svelte:component this={page} params={params} />
</main>

<style>
  .page {
    width: 100vw;
    height: calc(100vh - 52px);
    display: grid;
    grid-template-areas: 
      'menu main main main main'
  }
</style>