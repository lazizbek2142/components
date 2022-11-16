<script>
  export let color;
  export let active;
</script>

{#if active}
  <div class="badges" style="background-color: {color};" />
{/if}

<style>
  .badges {
    width: 1rem;
    height: 1rem;
    border-radius: 50%;
    position: absolute;
    z-index: 1000;
    top: 0;
    right: 0;
  }
</style>
