<script>
  import { Container, Row, Col, Button } from 'sveltestrap'

  const src = 'images/company-amico.png'
</script>

<style>
  .history-container {
    width: 100%;
    height: 100%;
    padding: 25px;
    margin-top: 30px;
    margin-bottom: 30px;
  }

  .history-content {
    color: #474646;
  }

  .history-content h1 {
    color: #1b9bff;
    font-size: 30px;
    font-weight: bold;
  }

  .img-section {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .history-content h2 {
    font-size: 20px;
    font-weight: bold;
  }
</style>

<div class="history-container">
  <Container>
    <Row xs="2">
      <Col>
        <div class="history-content">
          <h1>STARK TECHNOLOGIES INC.</h1>
          <h2>Company History</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
            pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
            culpa qui officia deserunt mollit anim id est laborum.
          </p>

          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Aliquet
            nec ullamcorper sit amet risus nullam eget. Duis ultricies lacus sed
            turpis. Iaculis nunc sed augue lacus viverra. Sodales ut etiam sit
            amet nisl purus. Morbi quis commodo odio aenean sed adipiscing diam
            donec adipiscing. Nunc mi ipsum faucibus vitae. Eget nunc
            scelerisque viverra mauris in. Proin sagittis nisl rhoncus mattis.
            Nullam non nisi est sit. Commodo nulla facilisi nullam vehicula.
            Viverra mauris in aliquam sem fringilla. Nibh tellus molestie nunc
            non. Porttitor leo a diam sollicitudin tempor id. Turpis massa sed
            elementum tempus egestas. Nunc vel risus commodo viverra. Vestibulum
            lorem sed risus ultricies tristique. Sagittis id consectetur purus
            ut faucibus pulvinar elementum integer. Sagittis orci a scelerisque
            purus semper eget.
          </p>
        </div>
      </Col>
      <Col>
        <div class="img-section">
          <img {src} alt="" style="width: 500px" />
        </div>
      </Col>
    </Row>
  </Container>
</div>
