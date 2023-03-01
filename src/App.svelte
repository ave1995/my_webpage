<script lang="ts">
  import Home from "./menu/Home.svelte";
  import Profile from "./menu/Profile.svelte";

  export let menu = 1;
</script>

<main>
  <div id="header">
    <span id="myname">Aleš Veselý</span>
    <ul id="menu">
      <li>
        <a href="/" on:click|preventDefault={() => (menu = 1)}>Home</a>
      </li>
      <li>
        <a href="/" on:click|preventDefault={() => (menu = 2)}>Profile</a>
      </li>
    </ul>
  </div>
  <div id="body">
    {#if menu === 1}
      <Home />
    {:else if menu === 2}
      <Profile />
    {:else}
      <h1>Page Not Found</h1>
    {/if}
  </div>
</main>

<style>
  #myname {
    display: inline;
    margin: 1rem;
    padding-left: 3.5rem;
    padding-right: 3.5rem;
    letter-spacing: 0.25rem;
    line-height: inherit;
    height: inherit;
    text-transform: uppercase;
    font-weight: 800;
  }
  #header {
    width: 100%;
    display: flex;
    justify-content: flex-start;
    border-color: white;
    border-bottom-style: solid;
    border-bottom-width: thin;
    position: relative;
    background-color: #202124;
  }
  ul#menu {
    margin: 0;
    padding: 1rem;
    padding-left: 2rem;
    border-color: white;
    border-left-style: solid;
    border-left-width: thin;
  }
  ul#menu li:not(:first-child) {
    border-color: white;
    border-left-style: solid;
    border-left-width: thin;
    padding-left: 1rem;
    margin-left: 1rem;
  }
  ul#menu li {
    display: inline;
  }

  ul#menu li a {
    color: white;
    text-decoration: none;
  }
  #body {
    margin: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border-color: white;
    border-style: solid;
    width: 50%;

  }
</style>
