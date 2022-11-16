<script>
  export let icon;
  export let color;
  export let to;
  export let radius;
  export let textColor;
  export let textSize;
</script>

{#if to}
  <a
    class="button"
    href={to}
    style="background-color: {color}; border-radius: {radius}; font-size: {textSize}; color: {textColor}"
  >
    <i class={icon} style="font-size: {textSize};" />
    <slot />
  </a>
{/if}
{#if !to}
  <button
    class="button"
    style="background-color: {color}; border-radius: {radius}; font-size: {textSize}; color: {textColor}"
  >
    <i class={icon} style="font-size: {textSize};" />
    <slot />
  </button>
{/if}

<style>
  .button {
    text-decoration: none;
    border: 0;
    width: fit-content;
    height: fit-content;
    display: block;
    text-align: center;
    justify-items: center;
    padding: 1rem;
    cursor: pointer;
  }
</style>
