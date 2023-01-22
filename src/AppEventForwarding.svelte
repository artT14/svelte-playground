<script>
	import Outer from "./components/Outer.svelte";
	function handleGreet(event){
		alert(event.detail)
	}
</script>

<main>
	<Outer on:greet={handleGreet}/>
</main>

<style>
	main {
		/* text-align: center; */
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>