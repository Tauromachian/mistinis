<template>
  <div>
    <section-hero></section-hero>

    <section-history></section-history>

    <section-races-carousel></section-races-carousel>

    <section-servers></section-servers>

    <section-server></section-server>

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
  font-family: 'poppins', sans-serif;
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
.hidden {
  display: none;
}

.container {
  max-width: 100%;
}

@media screen and (min-width: 576px) {
  .container {
    max-width: 540px;
    margin-right: auto;
    margin-left: auto;
  }
}

@media screen and (min-width: 768px) {
  .container {
    max-width: 720px;
  }
}

@media screen and (min-width: 992px) {
  .container {
    max-width: 960px;
  }
}

@media screen and (min-width: 1200px) {
  .container {
    max-width: 1140px;
  }
}

@media screen and (min-width: 1400px) {
  .container {
    max-width: 1320px;
  }
}

/* Hero section */

.servers__title-container {
  text-align: center;
}

button {
  background: #010101;
  color: white;
  border: none;
  width: 154.62px;
  height: 44.93px;
  cursor: pointer;
  background: #ad00ff;
  &:hover {
    box-shadow: 0px 0px 20px #ad00ff;
  }
}

/* Footer */
</style>
