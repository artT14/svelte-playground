<script>
	import ChildStyles from "./components/ChildStyles.svelte";
</script>

<main>
	<h3>App component global style</h3>
	<h4>App component text</h4>
	<ChildStyles/>
</main>

<style>
	:global(h3){
		color: blue;
	}
	h4 {
		color: orange;
	}
	main {
		/* text-align: center; */
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