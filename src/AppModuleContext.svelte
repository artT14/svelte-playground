<script>
    import Counter, {getTotalCount} from "./components/Counter.svelte";
</script>

<main>
    <button on:click={()=>{alert(getTotalCount())}}> Alert Total Count</button>
    <Counter />
    <Counter />
    <Counter />
</main>

<style>
</style>
