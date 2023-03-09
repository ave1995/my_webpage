<script lang="ts">
    import { activeStore } from "../../scripts/stores";
    import NavLink from "./NavLink.svelte";
</script>

<div class="header">
    <p>A\Ve</p>
    <nav class="navbar">
        <div>
            <div class="links">
                <NavLink keyword="Welcome" />
                <NavLink keyword="About" />
            </div>
        </div>
    </nav>
    <div></div>
</div>

<style>
    .header {
        grid-area: head;
        display: flex;
        align-items: center;
        background-color: #303136;
        justify-content: space-between;
    }
    .navbar {
        text-align: center;
    }
</style>
