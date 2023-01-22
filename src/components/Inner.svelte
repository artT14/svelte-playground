<script>
	import {createEventDispatcher} from 'svelte'
	import GreetButton from './GreetButton.svelte';
	const dispatch = createEventDispatcher();
	function greet(){
		dispatch("greet","hello")
	}
</script>
<GreetButton on:click={greet}/>