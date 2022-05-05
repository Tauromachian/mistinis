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
.footer-content {
  display: flex;
  position: relative;
  h2 {
    font-size: 4rem;
    font-weight: bold;
  }
  h3 {
    color: #ad00ff;
    font-weight: 500;
    font-size: 3.2rem;
    margin-bottom: 0.8em;
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
    z-index: 10;
    padding: 10em 0em 30em 0em;
    div {
      flex-basis: 50%;
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
