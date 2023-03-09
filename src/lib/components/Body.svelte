<script lang="ts">
    import { activeStore } from "../../scripts/stores";
    import About from "../../routes/About.svelte";
    import Welcome from "../../routes/Welcome.svelte";
    import Sidebar from "./Sidebar.svelte";
</script>

<div class="content">
    <div class="post">
        {#if $activeStore === "Welcome"}
            <Welcome />
        {:else if $activeStore === "About"}
            <About />
        {/if}
    </div>
    <div class="sidebar">
        <Sidebar />
    </div>
</div>

<style>
    .content {
        grid-area: content;
        display: flex;
        flex-direction: row-reverse;
        padding: 3em;
    }
    .post {
        flex: 70%;
    }
    .sidebar {
        flex: 30%;
    }
</style>
