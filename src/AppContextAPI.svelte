<script>
	import {setContext} from "svelte"
	import ComponentC from "./components/ComponentC.svelte";
	const userName = "Artona"
	setContext("username-context",userName) //set global context key-val
</script>

<main>
	<h2>App Component username - {userName}</h2>
	<ComponentC/>
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