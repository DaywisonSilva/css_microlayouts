<script lang="ts">
    import Routes from "@router/routes.svelte";
</script>

<Routes />

<style>
    :global(html, body, ul, ol, h1, h2, h3, h4, h5, h6) {
        margin: 0;
        padding: 0;
        font-family: sans-serif;
    }

    :global(html, body) {
        background-color: #333;
        height: 100vh;
        display: grid;
        place-content: center;
    }

    :global(ul, ol) {
        list-style: none;
    }

    :global(a) {
        text-decoration: none;
    }
</style>
