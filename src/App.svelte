<script lang="ts">
  import Home from "./menu/Home.svelte";
  import Profile from "./menu/Profile.svelte";

  export let menu = 1;
</script>

<main>
  <div id="header">
    <span id="myname">A\Ve</span>
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
   main {
    height: 100vh;
  }
  #myname {
    display: inline;
    margin: 1rem;
    padding-left: 3.5rem;
    padding-right: 3.5rem;
    letter-spacing: 0.25rem;
    line-height: inherit;
    height: inherit;
    font-weight: 600;
  }
  #header {
    width: 100%;
    display: flex;
    justify-content: flex-start;
    border-color:  #585b63;
    border-bottom-style: solid;
    border-bottom-width: thin;
    position: relative;
    background-color: #303136;
  }
  ul#menu {
    margin: 0;
    padding: 1rem;
    padding-left: 2rem;
    border-color:  #585b63;
    border-left-style: solid;
    border-left-width: thin;
  }
  ul#menu li:not(:first-child) {
    border-color:  #585b63;
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
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #585b63;
    border-radius: 10px;
    margin: auto;
    margin-top: 2rem;
    width: 50%;
    height: 50%;
    padding: 2rem;
    background-color: #303136;
  }
 
</style>
