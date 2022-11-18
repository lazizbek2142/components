<script>
  export let icon;
  export let color;
  export let to;
  export let radius;
  export let textColor;
  export let textSize;
  export let padding;
  export let active;
</script>

{#if to}
  <a
    class="button"
    href={to}
    style="background-color: {color}; border-radius: {radius}; font-size: {textSize}; color: {textColor}"
  >
    <i class={icon} style="font-size: {textSize}; padding: {padding}" />
    <slot />
  </a>
{/if}
{#if !to}
  <button
    class="button"
    style="background: {color}; border-radius: {radius}; font-size: {textSize}; color: {textColor}"
  >
    <i class={icon} style="font-size: {textSize}; padding: {padding}" />
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
    cursor: pointer;
    padding: 0;
  }
</style>
