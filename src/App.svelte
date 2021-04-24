<script>
import Body from "./Main/Body/Body.svelte";
import Rules from './Main/Rules/Rules.svelte';
import Router from 'svelte-spa-router';
const routes = {
	'/Rules': Rules,
	'*': Body,
};

</script>
<script context='module'>
	export let mainSection;

</script>
<style>
	main {
		height:100%;
		overflow-x: hidden;
	}
</style>
<svelte:head>
	<script src="https://kit.fontawesome.com/c0ff61a66a.js" crossorigin="anonymous"></script>
</svelte:head>
<main bind:this={mainSection}>
	<Router {routes}/>
</main>
