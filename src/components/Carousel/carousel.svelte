<script>
  import Carousel from '@beyonk/svelte-carousel'
  import { ChevronLeftIcon, ChevronRightIcon } from 'svelte-feather-icons'

  const Java = 'images/carousel/java.png'
  const Ruby = 'images/carousel/ruby.png'
  const Svelte = 'images/carousel/svelte.png'
  const Android = 'images/carousel/android.png'
  const Aws = 'images/carousel/aws.png'
  const Nodejs = 'images/carousel/nodejs.png'
  const Javascript = 'images/carousel/javascript.png'
  const React = 'images/carousel/react.png'
  const Redux = 'images/carousel/redux.png'
</script>

<style>
  .carousel-contanier {
    width: 100%;
    height: 400px;
    padding-top: 30px;
    padding-bottom: 50px;
    background: rgba(230, 227, 227, 0.322);
    position: relative;
  }

  .technologies {
    display: flex;
    text-align: center;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  .carousel-section {
    margin-top: 50px;
    padding: 20px;
  }

  .slide-content {
    width: 150px;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
  }

  .control :global(svg) {
    width: 100%;
    height: 100%;
    color: rgb(107, 107, 107);
    border: 2px solid rgb(107, 107, 107);
    border-radius: 32px;
  }

  h1 {
    padding: 15px;
    font-weight: 600;
    font-size: 25px;
    color: #474646;
  }

  p {
    font-size: 16px;
    color: #474646;
    text-align: center;
    line-height: 20px;
  }
</style>

<div class="carousel-contanier">
  <h1 class="technologies">Our technologies</h1>
  <p>
    Lorem Ipsum is simply dummy text of the printing and typesetting industry.
  </p>
  <div class="carousel-section">
    <Carousel
      easing="ease-out"
      dots
      loop
      autoplay={3000}
      duration={1000}
      perPage={{ 800: 6, 700: 5, 600: 4, 500: 3, 400: 2, 300: 2 }}>
      <span class="control" slot="left-control">
        <ChevronLeftIcon />
      </span>

      <img src={Java} class="slide-content" alt="" />
      <img src={Ruby} class="slide-content" alt="" />
      <img src={Svelte} class="slide-content" alt="" />
      <img src={Aws} class="slide-content" alt="" />
      <img src={Javascript} class="slide-content" alt="" />
      <img src={Nodejs} class="slide-content" alt="" />
      <img src={React} class="slide-content" alt="" />
      <img src={Redux} class="slide-content" alt="" />
      <img src={Android} class="slide-content" alt="" />

      <span class="control" slot="right-control">
        <ChevronRightIcon />
      </span>
    </Carousel>
  </div>
</div>
