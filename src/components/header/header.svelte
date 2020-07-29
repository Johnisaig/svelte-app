<script>
  import { navigate, link } from 'svelte-routing'
  const menuIcon = 'https://img.icons8.com/metro/26/000000/menu.png'

  let addName = ''
</script>

<style>
  .svelte-header {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
  }
  nav {
    background: #ffffff;
    box-shadow: 0 0 1px #ccc;
    height: 80px;
    width: 100%;
    position: fixed;
    z-index: 5;
  }
  label.logo {
    color: #474646;
    font-size: 33px;
    line-height: 80px;
    font-weight: 600;
    cursor: pointer;
    /* padding: 0 140px; */
    padding-left: 40px;
  }
  nav ul {
    float: right;
    margin-right: 30px;
  }
  nav ul li {
    display: inline-block;
    line-height: 80px;
    margin: 0 5px;
    text-align: center;
  }
  nav ul li a {
    color: #474646;
    font-weight: 500;
    font-size: 15px;
    padding: 5px 5px;
    border-radius: 3px;
    text-transform: uppercase;
    text-decoration: none;
  }

  a:hover {
    background: #1b9bff;
    color: #ffffff;
  }

  nav .current:active {
    background: #1b9bff;
    color: #ffffff;
  }

  .checkbtn {
    font-size: 30px;
    color: white;
    float: right;
    line-height: 80px;
    margin-right: 40px;
    cursor: pointer;
    display: none;
  }
  #check {
    display: none;
  }

  @media (max-width: 952px) {
    label.logo {
      font-size: 27px;
      padding-left: 25px;
    }
    nav ul li a {
      font-size: 16px;
      padding-right: 10px;
    }
    nav ul {
      margin-top: 0;
    }
  }
  @media (max-width: 858px) {
    .checkbtn {
      display: block;
      margin-right: 40px;
      z-index: 999;
    }
    ul {
      position: absolute;
      width: 100%;
      background: #2c3e50;
      top: 80px;
      left: -100%;
      text-align: center;
      transition: all 0.5s;
      z-index: 998;
    }
    nav ul li {
      display: block;
      margin: 50px 0;
      line-height: 30px;
    }
    nav ul li a {
      font-size: 20px;
      color: #ffffff;
    }

    #check:checked ~ ul {
      left: 0;
    }
  }
</style>

<header>
  <div class="svelte-header">
    <nav id="${addName}">
      <input type="checkbox" id="check" />
      <label for="check" class="checkbtn">
        <img src={menuIcon} alt="qwe" />
      </label>
      <label class="logo" on:click={() => navigate('/', { replace: true })}>
        STARK INC
      </label>
      <ul>
        <li>
          <a class="current" href="about" use:link replace>About</a>
        </li>
        <li>
          <a class="current" href="services" use:link replace>Services</a>
        </li>
        <li>
          <a class="current" href="career" use:link>Career</a>
        </li>
        <li>
          <a class="current" href="contact" use:link>Contact</a>
        </li>
      </ul>
    </nav>
  </div>
</header>
