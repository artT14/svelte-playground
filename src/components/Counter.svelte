<script context="module">
    let totalCount = 0
    export function getTotalCount() {
        return totalCount
    }
</script>

<script>
    let count = 0
    function clickHandler(){
        count++
        totalCount++
    }
</script>

<h2>Count is {count}</h2>
<button on:click={clickHandler}>Increment</button>