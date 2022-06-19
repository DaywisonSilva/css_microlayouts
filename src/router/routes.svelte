<script lang="ts">
  import Aside from '@components/molecules/Aside'
  import { Router, Route } from 'svelte-navigator'
</script>

<main>
  <Router>
    <Aside />
    <Route path="/">
      <h3>Home</h3>
      <p>Home sweet home...</p>
    </Route>
    <Route path="example1" />
    <Route path="example2">
      <h3>About</h3>
      <p>That's what it's all about!</p>
    </Route>
  </Router>
</main>

<!-- markup (zero or more items) goes here -->
<style>
  /* your styles go here */
</style>
