<script>
	import Videos from '../Videos.svelte';
	import Queue from '../Queue.svelte';

</script>


<main>
	
	<div class="vids">
		<Videos></Videos>
	</div> 

	<Queue></Queue>


</main>

<style>
	.vids{
		overflow-y:auto;
		box-sizing: border-box;
	}
	main {
		
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;

		display: grid;
		grid-gap: 10px;
		grid-template-rows: 1fr 60vh 2fr;

	}


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>