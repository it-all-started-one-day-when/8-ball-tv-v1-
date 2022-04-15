<script>
	import Videos from './Videos.svelte'
	import Banner from './Banner.svelte'
	import Header from './Header.svelte'
</script>
<Banner></Banner>
<Header></Header>
<main>
	

 <Videos>

</Videos> 


</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>