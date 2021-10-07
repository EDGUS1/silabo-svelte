<script>
  import { Router, Link, Route } from 'svelte-routing';
  import HomeSilabos from './HomeSilabos.svelte';

  import Login from './Login.svelte';
  export let url = '';
</script>

<Router {url}>
  <nav class="navbar navbar-expand-md navbar-light bg-light">
    <div class="container">
      <Link to="/" class="navbar-brand">Logo</Link>
      <button
        class="navbar-toggler collapsed"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarResponsive"
        aria-controls="navbarResponsive"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon" />
      </button>
      <div class="navbar-collapse collapse" id="navbarResponsive">
        <ul class="navbar-nav ms-md-auto">
          <li class="nav-item mx-3">
            <Link to="silabo" class="nav-link">Silabos</Link>
          </li>
          <li class="nav-item">
            <!-- <a class="btn btn-success" href="/" > Login </a> -->
            <button class="btn btn-danger"> Logout </button>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <div>
    <Route path="silabo" component={HomeSilabos} />
    <Route path="/"><Login /></Route>
  </div>
</Router>
