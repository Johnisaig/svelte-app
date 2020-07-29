<script>
  import { navigate, link } from 'svelte-routing'
  import { Button } from 'sveltestrap'

  export let title = 'Information Technology'
  export let src = ''
  export let description = ''
</script>

<style>
  .card-services-container {
    width: 100%;
    height: 600px;
    padding: 30px 20px 30px 20px;
    border: 1px solid #d6d6d6;
    text-align: center;
    margin-bottom: 30px;
  }

  .card-services-container:hover {
    box-shadow: 0 4px 19px 2px rgba(0, 0, 0, 0.3);
  }

  .services-first-column {
    height: 90%;
  }

  h1 {
    font-size: 20px;
    font-weight: 600;
    color: #474646;
    padding: 20px;
  }

  .services-second-column {
    bottom: 0;
    height: 100%;
    position: relative;
  }
</style>

<div class="card-services-container">
  <div class="services-first-column">
    <div>
      <img {src} alt="services" width="250px" />
    </div>

    <div>
      <h1>{title}</h1>
      <p>{description}</p>
    </div>
  </div>
  <div class="services-second-column">
    <Button
      color="primary"
      on:click={() => navigate('services', { replace: false })}>
      See More
    </Button>
  </div>
</div>
