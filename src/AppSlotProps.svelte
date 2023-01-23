<script>
	import NameList from "./components/NameList.svelte";
</script>

<main>
	<NameList>
		<h3 slot='hero' let:firstName let:lastName>
			{firstName} {lastName}
		</h3>
	</NameList>
	<NameList>
		<h3 slot='hero' let:firstName let:lastName>
			{lastName}, {firstName} 
		</h3>
	</NameList>
	<NameList>
		<h3 slot='hero' let:firstName let:lastName>
			{firstName} 
		</h3>
	</NameList>
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