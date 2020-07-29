<script>
  import WebRouter from './pages/routes/routes.svelte'
  import Header from '../src/components/header/header.svelte'
  import Footer from '../src/components/footer/footer.svelte'
</script>

<style>
  main {
    margin: 0;
    padding: 0;
    background-color: #fcfcfc;
  }
</style>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" />
</svelte:head>

<Header />
<main>
  <WebRouter />
</main>
<Footer />
