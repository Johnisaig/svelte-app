<script>
  export let name = ''
  export let src = ''
</script>

<style>
  .cardtitle-container {
    color: #ffffffe7;
    background: #0071bc;
    position: relative;
    padding-top: 100px;
  }

  .card-section {
    text-transform: capitalize;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 130px;
    top: -30px;
    position: relative;
  }

  .image-content {
    width: 30%;
    animation: image-section 2s;
  }

  .image-section {
    width: 100%;
    display: flex;
    justify-content: center;
    position: relative;
  }

  h1 {
    font-size: 40px;
    font-weight: bold;
    animation: animation 2s ease-in-out;
  }

  @keyframes image-section {
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

<div class="cardtitle-container">
  <div class="image-section">
    <img {src} alt="" class="image-content" />
  </div>
  <div class="card-section">
    <h1>{name}</h1>
  </div>
</div>
