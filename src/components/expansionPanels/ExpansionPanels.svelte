<script>
  import Button from "../Button.svelte";
  import PanelsNav from "./PanelsNav.svelte";
</script>

<div class="panels">
  <div class="panelsItem">
    <PanelsNav><slot /></PanelsNav>
    <Button />
  </div>
  <slot />
</div>

<style>
  .panels {
    width: 20rem;
    border: 1px solid;
    display: flex;
  }
</style>
