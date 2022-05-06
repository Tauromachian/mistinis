<template>
  <footer id="footer">
    <div class="container footer-content">
      <div class="footer-content-text">
        <h2>Turi klausimų?</h2>
        <h3>Susiek su mumis!</h3>
        <ul>
          <li>
            <i class="fa-solid fa-envelope"></i>
            MistinisPasaulis
          </li>
          <li><i class="fa-brands fa-facebook-f" />MistinisPasaulis</li>
          <li>
            <i class="fa-brands fa-discord"></i>
            MistinisPasaulis
          </li>
          <li>
            <i class="fa-brands fa-facebook"></i>
            MistinisPasaulis
          </li>
        </ul>
        <div><button>Anketa</button></div>
      </div>
      <img
        src="/images/rases_img/Pacaskurisapacioj.png"
        alt="An ugly ass goblin"
      />
    </div>
    <div class="copyright">
      <p>Visos teisės saugomos @MistinisPasaulis 2022</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
}
</script>

<style lang="scss" scoped>
footer {
  position: relative;

  &::before {
    z-index: 20;
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    background-color: rgb(0, 0, 0, 0.8);
  }
  @media screen and (min-width: 800px) {
    &::before {
      background-color: rgb(0, 0, 0, 0);
    }
  }
}

.footer-content {
  display: flex;
  position: relative;
  justify-content: center;
  text-align: center;

  @media screen and(min-width: 800px) {
    text-align: left;
    justify-content: left;
  }

  h2 {
    font-size: 2.5rem;
    font-weight: bold;
  }

  @media screen and(min-width: 800px) {
    h2 {
      font-size: 3.2rem;
      font-weight: bold;
    }
  }

  @media screen and(min-width: 1500px) {
    h2 {
      font-size: 4rem;
      font-weight: bold;
    }
  }

  h3 {
    color: #ad00ff;
    font-weight: 500;
    font-size: 2rem;
    margin-bottom: 0.8em;
  }

  @media screen and(min-width: 800px) {
    h3 {
      color: #ad00ff;
      font-weight: 500;
      font-size: 2.5rem;
      margin-bottom: 0.8em;
    }
  }

  @media screen and(min-width: 1500px) {
    h3 {
      color: #ad00ff;
      font-weight: 500;
      font-size: 3.2rem;
      margin-bottom: 0.8em;
    }
  }

  ul {
    list-style: none;
  }

  li {
    margin-top: 1em;
  }

  i {
    font-size: 1.4rem;
  }

  button {
    margin-top: 2em;
  }

  .footer-content-text {
    position: relative;
    z-index: 40;
    padding-top: 10em;
    padding-bottom: 10em;
    div {
      flex-basis: 50%;
    }
  }

  @media screen and(min-width: 800px) {
    .footer-content-text {
      padding: 5em 0em 20em 0em;
    }
  }

  @media screen and(min-width: 1500px) {
    .footer-content-text {
      padding: 10em 0em 30em 0em;
    }
  }

  img {
    z-index: 0;
    width: auto;
    height: 100%;
    position: absolute;
    right: 0;
  }
}

.copyright {
  padding: 15px;
  font-style: normal;
  font-size: 17px;
  line-height: 29px;
  text-align: center;
  color: white;
  background: black;
}
</style>
