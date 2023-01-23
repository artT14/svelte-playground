<script>
	import Card from "./components/Card.svelte";
</script>

<main>
	<Card>Card Content 1</Card>
	<Card><h2>Card Content 2</h2></Card>
	<Card><img alt src="https://picsum.photos/200"/></Card>
	<Card/>
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