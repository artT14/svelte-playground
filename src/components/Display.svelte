<script>
    import {count} from "../store/stores"
    // import { onDestroy } from "svelte";
    // let counter
    // const unsubscribe = count.subscribe((value)=>{counter=value})
    // onDestroy(unsubscribe)
    // //used to bind 'counter' in markup, now can reference store just by using $count
</script>

<h2>Current count is {$count}</h2>

