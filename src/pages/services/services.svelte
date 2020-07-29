<script>
  import CardTile from 'components/CardTitle/cardTitle.svelte'
  import ServicesCollapse from './components/services-collapse.svelte'
  import ServicesCollapse1 from './components/services-collapse1.svelte'
</script>

<style>
  .stark-services {
    margin: 0;
    position: relative;
    width: 100vw;
  }

  .content-container {
    width: 100%;
    height: 200px;
  }

  .Services-collpase-section {
    padding: 30px;
  }
</style>

<div class="stark-services">
  <CardTile name="Services" />
  <div class="Services-collpase-section">
    <ServicesCollapse title="Web and Mobile App" />
    <ServicesCollapse1 title=" Creative Branding" />
    <ServicesCollapse title="Web and Mobile App" />
  </div>
  <div class="content-container" />
</div>
