<template>
  <footer>
    <div class="container footer-content">
      <div>
        <h2>Turi klausimų?</h2>
        <h3>Susiek su mumis!</h3>
        <ul>
          <li><i class="fa-brands fa-facebook-f" />MistinisPasaulis</li>
          <li>
            <i class="fa-brands fa-discord"></i>
            MistinisPasaulis
          </li>
          <li>
            <i class="fa-brands fa-facebook"></i>
            MistinisPasaulis
          </li>
          <li>
            <i class="fa-solid fa-envelope"></i>
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
    <p id="copyright">Visos teisės saugomos @MistinisPasaulis 2022</p>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
}
</script>

<style lang="scss" scoped>
footer {
  padding-top: 10em;
}

.footer-content {
  display: flex;
  max-width: 800px;
}

.footer-content > div {
  flex-basis: 50%;
}

.footer-content h3 {
  color: #ad00ff;
}

.footer-content li {
  margin-top: 1em;
}

.footer-content button {
  margin-top: 2em;
}

.footer-content > img {
  width: 100%;
  height: auto;
}

ul {
  list-style: none;
}

ul > li {
}
</style>
