<script>
  import ItemCollapse from './collapse.svelte'

  import { navigate } from 'svelte-routing'
  import { Container, Collapse, Button, Row, Col } from 'sveltestrap'

  export let title = ''

  const src = 'images/services/business.png'

  import services1 from 'vars/services1.json'

  $: datas = services1.data

  let isOpen = false
</script>

<style>
  .business-container {
    width: 100%;
    padding: 30px;
  }

  .services-title {
    font-size: 35px;
    font-weight: bold;
    margin-bottom: 25px;
    color: #0071bc;
  }

  .services-section {
    align-items: center;
  }
</style>

<div class="business-container">
  <Container fluid>
    <Row sm="2">
      <Col lg="8">
        <div class="services-section">
          <div class="services-title">{title}</div>
          {#each datas as data (data.id)}
            <ItemCollapse
              servicesType={data.servicesType}
              servicesDesc={data.servicesDesc} />
          {/each}
        </div>
      </Col>
      <Col>
        <div>
          <img {src} alt="services" width="300" />
        </div>
      </Col>
    </Row>
  </Container>
</div>
