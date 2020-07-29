<script>
  import { Container, Row, Col } from 'sveltestrap'

  import CardTile from 'components/CardTitle/cardTitle.svelte'
  import CareerButton from 'components/Button/CareerButton.svelte'
  import History from './components/history.svelte'
  import Employee from './components/our-team.svelte'
  import employee from 'vars/employee.json'

  $: datas = employee.data
</script>

<style>
  .stark-about {
    margin: 0;
    position: relative;
    width: 100vw;
  }

  .content-container {
    width: 100%;
    height: 100px;
  }

  .about-our-employee h1 {
    width: 100%;
    color: #474646;
    font-weight: bold;
    text-align: center;
    padding: 20px;
  }

  .about-employee-section {
    width: 100%;
    height: 100%;
    padding-top: 20px;
    padding-bottom: 20px;
    display: flex;
    animation: animation 1s;
  }

  @keyframes animation {
    from {
      margin-top: 80px;
      opacity: 0.25;
    }
    to {
      margin-top: 0;
      opacity: 1;
    }
  }
</style>

<div class="stark-about">
  <CardTile name={'About Us'} />
  <History />
  <div>
    <div class="about-our-employee">
      <h1>Top Management</h1>
    </div>
    <div class="about-employee-section">
      <Container fluid>
        <Row lg="4">
          {#each datas as data (data.id)}
            <Col style="padding-bottom: 15px">
              <Employee
                src={data.image}
                position={data.position}
                fullname={data.fullname} />
            </Col>
          {/each}
        </Row>
      </Container>
    </div>
  </div>
  <CareerButton />
  <div class="content-container" />
</div>
