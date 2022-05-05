<template>
  <section class="hero">
    <header>
      <nav>
        <ul>
          <li><a href="#">Pagrindinis</a></li>
          <li><a href="#">Istorija</a></li>
          <li><a href="#">Rasės</a></li>
          <li><a href="#">Galerija</a></li>
          <li><a href="#">Kontaktai</a></li>
        </ul>
      </nav>
    </header>
    <div class="pagrindinis">
      <img id="logo" src="/images/logo.png" alt="" />
      <h5>
        Serverje žaidžia: <span style="font-weight: bold">25 žaidėjai</span>
      </h5>
      <div id="discord"><button>Discord</button></div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionHero',
}
</script>

<style lang="scss" scoped>
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
  width: 100%;
}

@media screen and (min-width: 540px) {
  #logo {
    width: 80%;
  }
}

@media screen and (min-width: 840px) {
  #logo {
    width: 60%;
  }
}

@media screen and (min-width: 1000px) {
  #logo {
    width: 40%;
  }
}

@media screen and (min-width: 1400px) {
  #logo {
    width: 30%;
  }
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
</style>
