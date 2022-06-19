<script lang="ts">
  import logo from './assets/svelte.png'
  import Aside from '@components/molecules/Aside'
  import Routes from '@router/routes'
</script>

<main class="main">
  <img src={logo} alt="Svelte Logo" />
  <Routes />
</main>

<style>
  :global(html, body, ul, ol, h1, h2, h3, h4, h5, h6) {
    margin: 0;
    padding: 0;
    font-family: sans-serif;
  }

  :global(ul, ol) {
    list-style: none;
  }

  img {
    height: 16rem;
    width: 16rem;
  }
</style>
