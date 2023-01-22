<script>
	const name = "Artavazd"
	const channel = "<b>Channel5 News</b>"
	const hack = `<a href="#" onclick="alert('You have been hacked!')">Win a Prize!</a>`
	const id = 'heading'
	const disabled = true
	const status = 'danger'
	const isPromoted = true
</script>

<main>
	<h2 class="underline">Underlined Text</h2>
	<h2 class={status}>Status</h2>
	<h2 class:promoted={isPromoted}>Movie Title</h2>
	<h1>Hello {name}!</h1>
	<div>{@html channel}</div>
	<div>{@html hack}</div>
	<h2 {id} {name}>This is a heading</h2>
	<button {disabled}> Bind </button>
</main>

<style>
	.underline{
		text-decoration: underline;
	}

	.danger{
		color: red;
	}

	.success{
		color: olive;
	}

	.promoted{
		font-style: italic;
	}

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