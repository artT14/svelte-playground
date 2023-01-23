<script>
	import Card2 from "./components/Card2.svelte";
</script>

<main>
	<Card2>
		<div slot='header'>
			<h3>Header</h3>
		</div>
		<div slot='content'>
			<img alt src="https://picsum.photos/200"/>
		</div>
		<div slot='footer'>
			<button>View Details</button>
		</div>
	</Card2>
	<Card2/>
	<Card2>
		<div slot='header'>
			<h3>Header</h3>
		</div>
		<div slot='content'>
			<img alt src="https://picsum.photos/200"/>
		</div>
	</Card2>
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