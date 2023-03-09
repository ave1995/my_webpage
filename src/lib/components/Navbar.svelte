<script lang="ts">
    import { activeStore } from "../../scripts/stores";
    import NavLink from "./NavLink.svelte";
</script>

<div class="header">
    <nav class="navbar">
        <div>
            <div class="links">
                <NavLink keyword="Welcome" />
                <NavLink keyword="About" />
            </div>
        </div>
    </nav>
</div>

<style>
    .header {
        grid-column: 1/4;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: #303136;
    }
</style>
