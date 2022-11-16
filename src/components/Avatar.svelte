<script>
  export let color;
  export let img;
  export let to;
</script>

<a href={to}>
  <div class="avatar" style="background-color: {color};">
    {#if !img}
      <i class="fa-solid fa-user" />
    {/if}
    {#if img}
      <img
        src={img}
        alt=""
        width="100%"
        height="100%"
        style="border-radius: 50%;"
      />
    {/if}
    <slot />
  </div>
</a>

<style>
  .avatar {
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    text-align: center;
    position: relative;
    cursor: pointer;
  }
  a {
    color: #000;
    text-decoration: none;
    display: inline-block;
    border-radius: 50%;
  }
  .avatar i {
    font-size: 2rem;
    margin-top: 0.8rem;
  }
</style>
