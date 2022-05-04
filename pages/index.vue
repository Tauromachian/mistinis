<template>
  <div>
    <section class="hero">
      <header>
        <div class="pagrindinisbg">
          <nav>
            <ul>
              <li><a href="#">Pagrindinis</a></li>
              <li><a href="#">Istorija</a></li>
              <li><a href="#">Rasės</a></li>
              <li><a href="#">Galerija</a></li>
              <li><a href="#">Kontaktai</a></li>
            </ul>
          </nav>
        </div>
      </header>
      <div class="pagrindinis">
        <img id="logo" src="/images/logo.png" alt="" />
        <h5>
          Serverje žaidžia: <span style="font-weight: bold">25 žaidėjai</span>
        </h5>
        <div id="discord"><button>Discord</button></div>
      </div>
    </section>

    <section-history></section-history>

    <section-races-carousel></section-races-carousel>

    <section-servers></section-servers>

    <app-footer> </app-footer>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss">
* {
  font-family: 'Poppins', sans-serif;
  color: white;
  margin: 0;
  padding: 0;
}

/* General styles */
body {
  background: url(/images/istorija.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
}

section {
  padding-top: 10em;
  padding-bottom: 10em;
}

/* Utility classes */
.container {
  max-width: 100%;
}

@media screen and (min-width: 640px) {
  .container {
    max-width: 610px;
    margin-right: auto;
    margin-left: auto;
  }
}

@media screen and (min-width: 768px) {
  .container {
    max-width: 728px;
  }
}

@media screen and (min-width: 1024px) {
  .container {
    max-width: 954px;
  }
}

@media screen and (min-width: 1280px) {
  .container {
    max-width: 1220px;
  }
}

@media screen and (min-width: 1536px) {
  .container {
    max-width: 1456px;
  }
}

/* Hero section */
.hero {
  padding-top: 0em;
  padding-bottom: 0em;
  height: 100vh;
  background: url(/images/test.jpg);
  background-repeat: no-repeat;
  background-size: 100% 100vh;
}

nav {
  text-align: center;
}

nav ul {
  display: flex;
  justify-content: center;
}

nav ul li {
  text-align: center;
  margin-top: 50px;
  list-style-type: none;
  width: 130px;
}

nav ul li a {
  text-decoration: none;
  color: inherit;
}

#logo {
  display: block;
  margin: 0 auto;
  width: 30%;
}

#discord {
  text-align: center;
}

h5 {
  text-align: center;
  font-weight: normal;
  font-size: 20px;
  margin-top: 0px;
  margin-bottom: 2%;
}

.servers__title-container {
  text-align: center;
}

#copyright {
  padding: 15px;
  font-style: normal;
  font-size: 17px;
  line-height: 29px;
  text-align: center;
  color: white;
  background: black;
}

button {
  background: #010101;
  color: white;
  border: none;
  width: 154.62px;
  height: 44.93px;
}

/* Footer */
</style>
