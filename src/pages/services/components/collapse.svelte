<script>
  import { navigate } from 'svelte-routing'
  import { Collapse, Button } from 'sveltestrap'

  export let servicesType = 'Business Consultation'
  export let servicesDesc = ''

  let isOpen = false
</script>

<style>
  .servicies-collapse {
    cursor: pointer;
    color: #474646;
  }

  h1 {
    font-size: 25px;
    font-weight: bold;
    color: #474646;
    margin-bottom: 20px;
  }
</style>

<div class="servicies-collapse" on:click={() => (isOpen = !isOpen)}>
  <div>
    <h1>{servicesType}</h1>
  </div>

  <Collapse {isOpen}>
    <div>
      <p>{servicesDesc}</p>
    </div>
    <Button
      color="primary"
      style="margin-top: 15px"
      on:click={() => navigate('/contact', { replace: true })}>
      GET A FREE QUATE
    </Button>
  </Collapse>
  <hr />
</div>
