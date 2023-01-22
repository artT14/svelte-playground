<script>
	const num = 5
</script>

<main>
	{#if num === 0}
	<h2>The number is zero</h2>
	{:else if num < 0}
	<h2>The number is negative</h2>
	{:else if num > 0}
	<h2>The number is positive</h2>
	{:else}
	<h2>Not a number</h2>
	{/if}
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