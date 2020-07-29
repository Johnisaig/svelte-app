<script>
  let programming = 'images/Web devices-amico.png'
  import Build from 'components/Button/Button.svelte'
</script>

<style>
  .build-with-us {
    display: flex;
    position: relative;
    width: 100%;
    height: 100%;
    align-items: center;
    justify-content: space-around;
    text-align: center;
    padding-top: 60px;
  }

  .content-image {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }

  .content-section {
    width: 100%;
    flex-wrap: wrap;
  }

  .content-image {
    width: 100%;
  }

  .img-dev {
    width: 95%;
    animation: animation 0.5s ease-in-out;
  }

  .content-text {
    margin: 15px;
    text-align: left;
    margin-bottom: 25px;
  }

  .text-heading {
    color: #1b9bff;
    animation: animation 0.5s ease-in-out;
  }

  .text-secondary {
    animation: animation 0.8s ease-in-out;
  }

  p {
    font-size: 18px;
  }

  h1 {
    font-size: 30px;
    font-weight: 30px;
  }

  @keyframes animation {
    0% {
      transform: scale(0.7);
    }
  }

  @media (max-width: 760px) {
    .build-with-us {
      flex-direction: column;
      align-items: center;
      text-align: center;
    }
  }
</style>

<div class="build-with-us">
  <div class="content-image">
    <img src={programming} alt="" class="img-dev" />
  </div>
  <div class="content-section">
    <div class="content-text">
      <h1 class="text-heading">WE ARE BUILDERS OF</h1>
      <h1 class="text-heading">MODERN APPLICATIONS</h1>
      <p class="text-secondary">
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry. Lorem Ipsum has been the industry's standard dummy text ever
        since the 1500s, when an unknown printer took a galley of type and
        scrambled it to make a type specimen book.
      </p>
    </div>
    <Build />

  </div>

</div>
