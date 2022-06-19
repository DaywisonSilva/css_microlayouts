<script>
  import { link } from 'svelte-navigator'
  let show = true
</script>

<aside class={show ? 'aside' : 'aside hidden'}>
  <button on:click={() => (show = false)}>close</button>
  <ul class="list">
    <a class="list__item" href="/" use:link>Home</a>
    <a class="list__item" href="example1" use:link>Example 1</a>
    <a class="list__item" href="example2" use:link>Example 2</a>
    <a class="list__item" href="example3" use:link>Example 3</a>
  </ul>
</aside>

<style>
  .aside {
    width: 200px;
    height: 100vh;
    background-color: red;
    position: fixed;
    top: 0;
    left: 0;
    transition: transform 0.3s ease-in-out;
  }

  .hidden {
    transform: translateX(-100%);
  }

  .list {
    width: 100%;
  }

  .list__item {
    display: block;
    width: 100%;
    color: white;
    text-align: center;
    margin: 20px 0;
    font-weight: bold;
    cursor: pointer;
    padding: 20px;
    box-sizing: border-box;
    transition: all 0.2s linear;
  }

  .list__item:hover {
    background-color: rgba(90, 2, 2, 0.639);
  }
</style>
