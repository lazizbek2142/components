<script>
  export let bgImage;
</script>

<div class="container" style="background-image: url({bgImage});">
  <slot />
</div>

<style>
  .container {
    width: 20rem;
    height: 25rem;
    border: 1px solid;
    box-shadow: inset;
    margin: 0 auto;
    font-family: Georgia, "Times New Roman", Times, serif;
    background-size: 100% 100%;
    display: flex;
    flex-direction: column;
  }
</style>
