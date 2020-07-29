<script>
  export let name = ''
</script>

<style>
  .cardtitle-container {
    background: #0071bc;
    color: #ffffffe7;
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
  }

  h1 {
    font-size: 40px;
    font-weight: bold;
  }
</style>

<div class="cardtitle-container">
  <div class="card-section">
    <h1>{name}</h1>
  </div>
</div>
