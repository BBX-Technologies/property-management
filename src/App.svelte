<script>
	import { fade, fly } from 'svelte/transition';
	import './global.scss';
	import Navbar from './components/Navbar.svelte';
	import Page  from './Page.svelte';
	import LoginForm from './components/LoginForm.svelte';
	import Welcome from './components/Welcome.svelte';
	import { loggedIn } from './area/User/store.js'
</script>

<Page />
<!-- <div class="container">
	{#if $loggedIn}
	<div in:fly="{{ y: 1000, duration: 2000 }}">
		<Welcome/>
	</div>
	{:else}
	<div out:fade>
		<LoginForm />
	</div>
	{/if}
</div> -->
