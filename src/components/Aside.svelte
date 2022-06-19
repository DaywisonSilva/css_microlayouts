<script>
    import { link } from "svelte-navigator";
    import { createEventDispatcher } from "svelte";
    const dispatcher = createEventDispatcher();

    export let show;
</script>

<aside class={show ? "aside" : "aside hidden"}>
    <button class="aside__btn" on:click={() => dispatcher("hide", false)} />
    <ul class="list">
        <a
            class="list__item"
            href="/"
            use:link
            on:click={() => dispatcher("hide", false)}>Home</a
        >
        <a
            class="list__item"
            href="example1"
            use:link
            on:click={() => dispatcher("hide", false)}>Example 1</a
        >
        <a
            class="list__item"
            href="example2"
            use:link
            on:click={() => dispatcher("hide", false)}>Example 2</a
        >
        <a
            class="list__item"
            href="example3"
            use:link
            on:click={() => dispatcher("hide", false)}>Example 3</a
        >
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
        padding-top: 50px;
        z-index: 1;
        box-shadow: 5px 0 40px rgba(34, 34, 34, 0.893);
    }

    .aside__btn {
        width: 40px;
        height: 40px;
        border: 2px solid #333;
        border-radius: 8px;
        position: absolute;
        top: 20px;
        right: 20px;
        cursor: pointer;
    }
    .aside__btn::before,
    .aside__btn::after {
        content: "";
        display: block;
        width: 25px;
        height: 3px;
        border-radius: 2px;
        background-color: black;
    }

    .aside__btn::after {
        transform: rotate(45deg) translateY(-1px);
    }

    .aside__btn::before {
        transform: rotate(-45deg) translateY(1px);
    }

    .hidden {
        transform: translateX(-100%);
        box-shadow: none;
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

    @media screen and (min-width: 800px) {
        .aside {
            width: 280px;
        }
    }
</style>
