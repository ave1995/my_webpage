<script lang="ts">
    import { _ } from "svelte-i18n";
    import { activeStore } from "../../scripts/stores";
    export let keyword: string;

    const setActive = () => {
        $activeStore = keyword;
    };
</script>

<button class:active={$activeStore == keyword} on:click={setActive}>
    <span>{$_(`navbar.${keyword}`)}</span>
</button>

<style>
    button {
        border: none;
        background-color: inherit;
        text-decoration: none;
        color: hsla(0, 0%, 100%, 0.4);
        font-size: inherit;
        font-family: inherit;
    }
    button span:after {
        display: block;
        content: "";
        border-bottom: solid 3px #f8f9fa;
        transform: scaleX(0);
        transform-origin: bottom right;
        transition: transform 250ms ease-out;
    }
    .active span {
        color: #f8f9fa;
        border-bottom: solid 3px #f8f9fa;
    }
    button:hover {
        cursor: pointer;
        color: #f8f9fa;
        transition: color 1s ease-out;
    }
    button:not(.active) span:hover:after {
        transform: scaleX(1);
        transform-origin: bottom left;
    }
</style>
