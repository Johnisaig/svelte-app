<script>
  import { link } from 'svelte-routing'
  import {
    FacebookIcon,
    TwitterIcon,
    InstagramIcon,
    YoutubeIcon,
  } from 'svelte-feather-icons'

  const StarkLogo = 'images/stark.png'
</script>

<style>
  footer {
    color: #f7f7f7;
    clear: both;
    position: relative;
    bottom: 0;
    padding: 10px;
    box-sizing: border-box;
    background: rgb(29, 29, 29);
  }

  .footer-container {
    bottom: 0;
    margin: 20px;
    position: relative;
    height: 100%;
  }

  a {
    text-decoration: none;
  }

  ul {
    text-decoration: none;
    list-style: none;
    padding: 0px;
  }

  .footer-up-section {
    margin: 0px;
    padding: 0px;
  }

  .footer-up-section h1 {
    font-size: 18px;
  }

  .footer-up-section ul li a {
    font-size: 13px;
    color: #575a70;
  }

  .footer-up-section ul li p {
    font-size: 14px;
    color: #575a70;
  }

  .footer-up-section {
    padding-bottom: 55px;
    border-bottom: 1px solid #3a3b3b8a;
  }

  .footer-up-section,
  .footer-down-section {
    display: flex;
    justify-content: space-between;
    width: 100%;
    flex-wrap: wrap;
  }

  .social-icons a {
    width: 35px;
    height: 35px;
    margin: 0 5px;
    background: #424356;
    box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1);
    display: flex;
    justify-content: center;
    align-items: center;
    color: #ffffff;
  }

  .social-icons {
    display: flex;
  }

  .footer-down-section {
    bottom: 0;
    margin-top: 25px;
    margin-bottom: 10px;
    position: relative;
  }

  .stark-logo {
    width: 100px;
  }

  .copyright-section {
    color: #5c5c5c;
    font-size: 11px;
  }

  @media (max-width: 760px) {
    .footer-up-section {
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .footer-up-section {
      padding-bottom: 25px;
    }
  }
</style>

<footer>
  <div class="footer-container">
    <div class="footer-up-section">
      <section>
        <h1>ABOUT US</h1>
        <ul>
          <li>
            <a class="active" href="/" use:link>Vision & Mission</a>
          </li>
          <li>
            <a href="about" use:link>Our Expertise</a>
          </li>
          <li>
            <a href="services" use:link>Technologies & Delivert Process</a>
          </li>
          <li>
            <a href="contact" use:link>Management</a>
          </li>
          <li>
            <a href="portfolio" use:link>Privacy Policy</a>
          </li>
        </ul>
      </section>

      <section>
        <h1>PROJECTS</h1>
        <ul>
          <li>
            <a class="active" href="/" use:link>ARTICLES</a>
          </li>
        </ul>
      </section>

      <section>
        <h1>CAREERS</h1>
        <ul>
          <li>
            <a class="active" href="/" use:link>Life at Stark Inc</a>
          </li>
          <li>
            <a href="about" use:link>Job Openenings</a>
          </li>
        </ul>
      </section>

      <section>
        <h1>CONTACT US</h1>
        <ul>
          <li>
            <p>example@example.com</p>
          </li>
          <li>
            <p>+123123123123</p>
          </li>
        </ul>
      </section>

      <section class="social">
        <h1>SOCIALS</h1>
        <div class="social-icons">
          <a class="active" href="/" use:link>
            <FacebookIcon size="14" />
          </a>

          <a class="active" href="/" use:link>
            <TwitterIcon size="14" />
          </a>

          <a class="active" href="/" use:link>
            <InstagramIcon size="14" />
          </a>

          <a class="active" href="/" use:link>
            <YoutubeIcon size="14" />
          </a>
        </div>
      </section>

    </div>
    <div class="footer-down-section">
      <div class="company-logo-section">
        <img src={StarkLogo} alt="" class="stark-logo" />
      </div>
      <div class="copyright-section">
        <p>© Copyright 2020 StarkTechnologies, Inc. All rights reserved.</p>
      </div>
    </div>
  </div>
</footer>
