<script>
  import { Button, Input, Container, Row, Col, FormGroup } from 'sveltestrap'
</script>

<style>
  h1 {
    font-size: 16px;
    color: #444;
    font-weight: 500;
  }
</style>

<div class="apply-container">
  <FormGroup row>
    <Col sm={6}>
      <h1>Name</h1>
      <Input />
    </Col>
    <Col sm={6}>
      <h1>Email</h1>
      <Input type="email" />
    </Col>
  </FormGroup>

  <FormGroup row>
    <Col sm={6}>
      <h1>Position</h1>
      <Input type="select">
        <option>Senior. Software Engineer</option>
        <option>Android Developer</option>
        <option>Fron-End Developer</option>
        <option>Back-End Developer</option>
        <option>IOS Developer</option>
      </Input>
    </Col>
    <Col sm={6}>
      <h1>Resume</h1>
      <Input type="file" />
    </Col>
  </FormGroup>

  <FormGroup row>
    <Col>
      <h1>Cover Letter</h1>
      <Input type="textarea" name="text" rows="5" />
    </Col>
  </FormGroup>

  <div>
    <Button size="md" color="primary">SUMMIT APPLICATION</Button>
  </div>

</div>
