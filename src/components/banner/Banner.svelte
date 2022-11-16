<script>
  import BannerText from "./BannerText.svelte";
  import Action from "../Action.svelte";
</script>

<div class="container">
  <slot />
  <div class="bannerContent">
    <BannerText
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, quod!</BannerText
    >
    <Action position={"end"}><button>click</button></Action>
  </div>
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
  }
  .bannerContent {
    display: flex;
    flex-direction: column;
    text-align: center;
    width: 80%;
    margin-top: 2rem;
  }
</style>
