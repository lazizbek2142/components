<script>
  export let text;
  export let title;
  export let readonly;

  let active = false;
  const activated = function () {
    if (!readonly) {
      active = !active;
    }
  };
</script>

<div class={!active ? "panel" : "panel-active"}>
  <div class={active ? "title open" : "title"} on:click={activated}>
    <h4>{title}</h4>
    <i class={active ? "fa-solid fa-angle-up" : "fa-solid fa-angle-down"} />
  </div>
  <div class={active ? "content active" : "content"}>
    <p>{text}</p>
  </div>
</div>

<style>
  .panel {
    width: 100%;
    overflow: hidden;
    box-shadow: 0 1px 1px rgba(185, 178, 178, 0.547);
    margin-bottom: 0.5px;
  }
  .panel-active {
    width: 100%;
    overflow: hidden;
    margin-bottom: 5px;
    box-shadow: 0 1px 1px rgba(185, 178, 178, 0.547);
    transition: 0.5s;
    border-radius: 7px;
  }

  .title {
    background: #fff;
    display: flex;
    justify-content: space-between;
    padding: 0 20px;
    align-items: center;
    transition: 0.5s;
  }
  .title:hover {
    background: rgba(185, 178, 178, 0.547);
  }

  .title * {
    margin: 10px 0;
  }

  .open {
    padding: 10px 20px;
    transition: 0.5s;
    background: rgb(169, 170, 172);
  }
  .content {
    height: 0;
    padding: 0 20px;
    transition: 0.5s;
  }
  .content * {
    margin: 0;
  }
  .active {
    height: fit-content;
    padding: 20px 20px;
    transition: 0.5s;
  }
  .active p {
    height: fit-content;
    position: relative;
    z-index: -1;
  }
</style>
