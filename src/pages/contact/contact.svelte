<script>
  import CardContent from 'components/CardContent/card-content.svelte'
  import { Input, Container, Row, Col, Button } from 'sveltestrap'
</script>

<style>
  .stark-contact {
    margin: 0;
    position: relative;
    width: 100%;
  }

  .content-container {
    height: auto;
    margin: 50px;
    align-items: center;
    position: relative;
  }

  .form-heading h1 {
    color: #474646;
    font-weight: bold;
    font-size: 30px;
    margin-bottom: 50px;
  }

  .content-container span {
    color: #474646;
    font-size: 18px;
    font-weight: 600;
  }

  .contact-location span {
    color: #1b9bff;
    font-size: 18px;
    margin-bottom: 50px;
  }

  .contact-location h2 {
    color: #474646;
    font-size: 16px;
    margin-top: 20px;
    line-height: 25px;
  }

  .form-input-section {
    margin-bottom: 20px;
  }
</style>

<div class="stark-contact">
  <CardContent src="images/contact-us.png" name="Feel Free to get in touch." />
  <div class="content-container">
    <Container fluid>
      <Row xs="2">
        <Col lg="8" style="padding-bottom: 35px">
          <div class="">
            <div class="form-heading">
              <h1>Do you have something in mind? Let’s discuss!</h1>
            </div>

            <div class="form-input-section">
              <div>
                <span>Name*</span>
                <Row>
                  <Col>
                    <Input placeholder="First name" />
                  </Col>
                  <Col>
                    <Input placeholder="Last name" />
                  </Col>
                </Row>
              </div>
            </div>

            <div class="form-input-section">
              <Row>
                <Col>
                  <span>E-mail*</span>
                  <Input />
                </Col>
              </Row>
            </div>

            <div class="form-input-section">
              <Row>
                <Col>
                  <span>Subject *</span>
                  <Input />
                </Col>
              </Row>
            </div>

            <div class="form-input-section">
              <Row>
                <Col>
                  <span>Comment or Message *</span>
                  <Input type="textarea" name="text" rows="7" />
                </Col>
              </Row>
            </div>
            <div>
              <Row>
                <Col>
                  <Button color="primary">Send Message</Button>
                </Col>
              </Row>
            </div>
          </div>
        </Col>

        <Col>
          <div class="contact-location">
            <div>
              <span>ADDRESS</span>
              <h2>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore magna aliqua
              </h2>
            </div>

            <div>
              <span>CONTACT</span>
              <h2>Tel: +63123123123 | +631 1233 1233​</h2>
              <h2>Email: Example@example.com</h2>
              <h2>Recruitment: hr@stark.com​</h2>
            </div>
          </div>
        </Col>
      </Row>
    </Container>
  </div>
</div>
