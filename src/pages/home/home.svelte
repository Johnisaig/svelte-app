<script>
  import { Container, Row, Col } from 'sveltestrap'

  import BuildWithUs from './components/build.svelte'
  import Inspire from './components/inspire.svelte'
  import Carousel from 'components/Carousel/carousel.svelte'
  import Services from 'components/CardServices/card-services.svelte'

  import jsonServices from 'vars/services.json'

  $: datas = jsonServices.data
</script>

<style>
  .sercives-container {
    width: 100%;
    padding: 30px;
    position: relative;
    text-align: center;
  }

  .sercives-section h1 {
    font-size: 35px;
    font-weight: bold;
    color: #474646;
    padding: 30px;
  }
</style>

<div>
  <BuildWithUs />
  <Inspire />
  <div class="sercives-container">
    <div class="sercives-section">
      <h1>Our Services</h1>
    </div>
    <Container fluid>
      <Row sm="3">
        {#each datas as data (data.id)}
          <Col>
            <Services
              src={data.image}
              title={data.title}
              description={data.description} />
          </Col>
        {/each}
      </Row>
    </Container>
  </div>
  <Carousel />
</div>
