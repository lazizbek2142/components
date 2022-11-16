<script>
  export let img;
</script>

<div class="container" style="background-image: url({img});">
  <div class="buttons">
    <slot />
  </div>
</div>

<style>
  .container {
    margin: 0 auto;
    width: 50rem;
    height: 30rem;
    position: relative;
    background-size: 100% 100%;
  }
  .buttons {
    display: flex;
    justify-content: space-between;
    width: 95%;
    margin: 0 auto;
    transform: translateY(400%);
  }
</style>
