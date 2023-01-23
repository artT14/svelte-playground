<script>
    import TabA from "./components/TabA.svelte";
    import TabB from "./components/TabB.svelte";
    import TabC from "./components/TabC.svelte";
    let activeTab = TabA
</script>

<main>
    <button on:click={()=>(activeTab = TabA)}>Tab A</button>
    <button on:click={()=>(activeTab = TabB)}>Tab B</button>
    <button on:click={()=>(activeTab = TabC)}>Tab C</button>
    <svelte:component this={activeTab}></svelte:component>
    <!-- {#if activeTab == 'TabA'}
    <TabA/>
    {/if}
    {#if activeTab == 'TabB'}
    <TabB/>
    {/if}
    {#if activeTab == 'TabC'}
    <TabC/>
    {/if} -->
</main>

<style>
</style>
