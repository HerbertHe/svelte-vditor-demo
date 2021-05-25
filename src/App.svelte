<script>
    import { onMount } from "svelte"
    import Vditor from "vditor"

    onMount(() => {
        const vditor = new Vditor("vditor-container", {
            theme: "classic",
            minHeight: 600,
        })
    })
</script>

<h1>Vditor Demo For Svelte</h1>

<div id="vditor-container" />

<style>
    h1 {
        color: #ff3e00;
    }
</style>
