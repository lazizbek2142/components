<script>
  export let position;
</script>

<div class="action" style="text-align: {position};">
  <slot />
</div>

<style>
  .action {
    padding: 0.5rem;
    align-content: space-around;
  }
</style>
