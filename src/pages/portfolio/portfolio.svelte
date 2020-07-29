<script>
  import CardTile from 'components/CardTitle/cardTitle.svelte'
</script>

<style>
  .stark-portfolio {
    margin: 0;
    position: relative;
    width: 100vw;
  }

  .content-container {
    width: 100%;
    height: 200px;
  }
</style>

<div class="stark-portfolio">
  <CardTile name="portfolio" />
  <div class="content-container" />
</div>
