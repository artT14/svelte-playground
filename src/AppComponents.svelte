<script>
	import Greet from "./components/Greet.svelte";
	$: name = "Vazart"
	$: surname = "Rosoti"
	const mom = {
		name: "Armia",
		surname: "Rosoti"
	}
</script>

<main>
	<button on:click={()=>{name="Tiger"}}>Change Name</button>
	<Greet {name} {surname}/>
	<Greet name="Alfonso" {surname}/>
	<Greet name="Shargit" {surname}/>
	<Greet/>
	<Greet {...mom}/>
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