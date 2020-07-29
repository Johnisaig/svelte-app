<script>
  import {
    Card,
    CardImg,
    CardText,
    CardBody,
    CardTitle,
    CardSubtitle,
  } from 'sveltestrap'

  export let fullname = 'John Doe'
  export let position = 'Front-End / Software Engineer'
  export let src = 'images/careers.jpg'
  const arrowRight = 'images/arrow-right-icon.png'
</script>

<style>
  .our-team-container {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    color: #474646;
    cursor: pointer;
  }

  .card-content {
    width: 250px;
  }

  #arrow-icon {
    width: 20px;
    transition: transform 1s;
  }

  .lbl-fullname {
    font-size: 23px;
    font-weight: 600;
  }

  #zoom-animation {
    transition: transform 1s;
  }

  .card-content:hover #zoom-animation {
    transform: scale(0.9);
  }

  .card-content:hover #arrow-icon {
    transform: scale(1.2);
  }
</style>

<div class="our-team-container">
  <div class="card-content">
    <Card>
      <div id="zoom-animation">
        <CardImg style="width: 100%; height: 300px;" {src} alt="" />
      </div>
      <CardBody>
        <div>{position}</div>
        <div class="lbl-fullname">{fullname}</div>
        <div id="arrow-icon">
          <img src={arrowRight} alt="" />
        </div>
      </CardBody>
    </Card>
  </div>
</div>
