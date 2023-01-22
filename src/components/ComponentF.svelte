<script>
	import {getContext} from "svelte"
	let userName = getContext("username-context") //get global context key-val
</script>
<h2>Child Component F</h2>
<h2>Child Component F - userName - {userName}</h2>