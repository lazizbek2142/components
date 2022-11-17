<script>
  import BannerText from "./BannerText.svelte";
  import Action from "../Action.svelte";
</script>

<div class="container">
  <slot />
</div>

<style>
  .container {
    width: 50rem;
    height: fit-content;
    border: 1px solid;
    display: flex;
    align-items: center;
    margin: 0 auto;
    justify-content: space-between;
    padding: 1rem;
  }
</style>
