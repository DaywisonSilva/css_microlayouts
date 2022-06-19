<script lang="ts">
    import Aside from "@components/Aside.svelte";
    import Home from "@views/Home.svelte";

    let showDrawer = false;
    import { Router, Route } from "svelte-navigator";
</script>

<Router>
    <button class="btn btn__open" on:click={() => (showDrawer = true)} />
    <Aside show={showDrawer} on:hide={(event) => (showDrawer = event.detail)} />
    <main>
        <Route path="/">
            <div class="animate__animated animate__slideInLeft">
                <Home />
            </div>
        </Route>
        <Route path="example1">
            <div class="animate__animated animate__slideInLeft">
                Primeira rota porra
            </div>
        </Route>
        <Route path="example2">
            <div class="animate__animated animate__slideInLeft">
                <h3>About</h3>
                <p>That's what it's all about!</p>
            </div>
        </Route>
        <Route path="example3">
            <div class="animate__animated animate__slideInLeft">
                <h3>About</h3>
                <p>Exemplo 3</p>
            </div>
        </Route>
    </main>
</Router>

<!-- markup (zero or more items) goes here -->
<style>
    .btn {
        width: 40px;
        height: 40px;
        border: 2px solid #333;
        border-radius: 8px;
        position: absolute;
        top: 20px;
        left: 20px;
        cursor: pointer;
    }
    .btn__open::before,
    .btn__open::after {
        content: "";
        display: block;
        width: 25px;
        height: 3px;
        border-radius: 2px;
        background-color: #222;
    }

    .btn__open::after {
        margin-top: 4px;
        width: 18px;
    }
    .btn__open::before {
        margin-bottom: 4px;
    }
</style>
