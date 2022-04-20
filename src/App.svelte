<script>
	import Router from 'svelte-spa-router';
	import Home from './routes/Home.svelte';
	import About from './routes/About.svelte';
	import Video from './routes/Video.svelte';
	import Notfound from './routes/Notfound.svelte';

	import Videos from './Videos.svelte';
	import Banner from './Banner.svelte';
	import Header from './Header.svelte';
	import Queue from './Queue.svelte';


	let routes = {
			"/": Home,
			"/about": About,
			"/video/:id": Video,


			"*": Notfound

	};

</script>

<Banner></Banner>
<Header></Header>

<main>
	<Router {routes}/>
	

</main>

<style>

</style>