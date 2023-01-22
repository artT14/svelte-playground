<script>
	const names = ['Art', 'Albert', 'Serzh', 'Gev', 'Rud']
	const fullNames = [
		{first: 'Bruce', last: 'Willis'},
		{first: 'Bob', last: 'Vance'},
		{first: 'Kurt', last: 'Cobain'}
	]
</script>

<main>
	{#each fullNames as name, id (name.last)}
	<h2 {id}>{name.first} {name.last}</h2>
	{/each}

	{#each names as name, id (name)}
	<h2 {id}>{name}</h2>
	{/each}
</main>

<style>
	main {
		text-align: center;
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