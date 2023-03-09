<script lang="ts">
  import { getLocaleFromNavigator, init, addMessages } from "svelte-i18n";

  import en from "../localization/en.json";

  addMessages("en", en);

  init({
    fallbackLocale: "en",
    initialLocale: getLocaleFromNavigator(),
  });

  import Navbar from "./lib/components/Navbar.svelte";

  import Footer from "./lib/components/Footer.svelte";

  import Body from "./lib/components/Body.svelte";
</script>

<main>
  <div class="container">
    <Navbar />
    <Body />
    <Footer />
  </div>
</main>

<style>
</style>
