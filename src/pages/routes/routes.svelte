<script>
  import { Router, Route } from 'svelte-routing'
  import Home from '../home/home.svelte'
  import Services from '../services/services.svelte'
  import Career from '../career/career.svelte'
  import Contact from '../contact/contact.svelte'
  import About from '../about/about.svelte'
  export let url = ''
</script>

<Router {url}>
  <Route path="services" component={Services} />
  <Route path="career" component={Career} />
  <Route path="contact" component={Contact} />
  <Route path="about" component={About} />
  <Route path="/">
    <Home />
  </Route>
</Router>
