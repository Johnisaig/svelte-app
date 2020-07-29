<script>
  export let title = 'LOREM IPSUM TITLE'
  export let company = 'STARK'
</script>

<style>
  .inspire-container {
    width: 100%;
  }

  .inspire-title {
    padding: 20px 20px 0 20px;
    text-align: center;
  }

  .inspire-content {
    padding: 10px 40px;
    text-align: center;
  }

  h1 {
    font-size: 40px;
    font-weight: 600;
    font-style: normal;
    color: #1b9bff;
    animation: animation 2s ease-in-out;
    animation: animation ease 4s;
  }

  p {
    color: #474646;
    font-size: 18px;
    font-weight: 600px;
    font-style: normal;
  }

  @keyframes animation {
    from {
      margin-right: 100%;
      width: 300%;
    }
    to {
      margin-right: 0%;
      width: 100%;
    }
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
</style>

<div class="inspire-container">
  <div class="inspire-title">
    <h1>{title}</h1>
  </div>
  <div class="inspire-content">
    <p>
      <strong>{company}</strong>
      is a
      <strong>TRANSFORMATION ENABLER</strong>
      delivering
      <strong>ENTERPRISE-GRADE SOLUTIONS</strong>
      globally for more than 20 years. We specialize in providing Agile Software
      Development, Cloud, Data Engineering and AI services.
    </p>
    <p>
      Lorem Ipsum is simply dummy text of the printing and typesetting industry.
      Lorem Ipsum has been the industry's standard dummy text ever since the
      1500s, when an unknown printer took a galley of type and scrambled it to
      make a type specimen book.
    </p>
  </div>
</div>
