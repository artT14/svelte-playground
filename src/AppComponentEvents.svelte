<script>
	import Popup from "./components/Popup.svelte";

	let showPopup = false
	function closePopUp(event){
		showPopup=false
		console.log(event.detail) //data coming from child
	}
</script>

<main>
	<button on:click={()=>(showPopup=true)}>Open Popup</button>
	{#if showPopup}
		<Popup on:close={closePopUp}/>
	{/if}
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