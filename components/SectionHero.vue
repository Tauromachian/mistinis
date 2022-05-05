<template>
  <section class="hero">
    <header>
      <nav v-if="!isScreenSmall">
        <ul>
          <li v-for="(link, index) in links" :key="`link-${link}-${index}`">
            <a :href="link.url">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
      <div v-else>
        <button class="modal-open-button" @click="openModal">
          <i class="fa-solid fa-bars"></i>
        </button>
        <div id="modal">
          <nav class="modal-nav">
            <ul class="modal-links">
              <li
                v-for="(link, index) in links"
                :key="`modal-link-${link}-${index}`"
              >
                <a :href="link.url">{{ link.text }}</a>
              </li>
            </ul>
          </nav>
          <button
            class="modal-close-button position-absolute"
            @click="closeModal"
          >
            <i class="fa-solid fa-xmark"></i>
          </button>
        </div>
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
</template>

<script>
export default {
  name: 'SectionHero',
  data() {
    return {
      modal: {},
      body: {},
      width: '',
      links: [
        { text: 'Pagrindis', url: '#' },
        { text: 'Istorija', url: '#section-history' },
        { text: 'Rasės', url: '#section-races-carousel' },
        { text: 'Galerija', url: '#section-servers' },
        { text: 'Kontaktai', url: '#footer' },
      ],
    }
  },
  computed: {
    isScreenSmall() {
      return this.width < 991
    },
    path() {
      return this.$nuxt.$route.name
    },
    logo() {
      const routeName = this.$nuxt.$route.name
      if (routeName === 'repair' || routeName === 'service') {
        return '/JTRS-min.png'
      }
      return '/johnson-logo-min.png'
    },
  },
  mounted() {
    this.modal = document.getElementById('modal')
    this.body = document.body
    this.closeModal()
    this.width = window.innerWidth
    window.addEventListener('resize', () => {
      this.width = window.innerWidth
    })
  },

  methods: {
    openModal() {
      this.modal.style.display = 'block'
      this.body.style.overflow = 'hidden'
    },
    closeModal() {
      this.modal.style.display = 'none'
      this.body.style.overflow = 'unset'
    },
  },
}
</script>

<style lang="scss" scoped>
button {
  cursor: pointer;
}

.hidden {
  display: none;
}

#modal {
  display: none;
  position: fixed;
  background-color: rgb(14, 13, 13);
  width: 100vw;
  height: 100vh;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: 1000;
}

.modal-nav {
  height: 100%;
}

.modal-links {
  display: flex;
  height: 100%;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.modal-open-button,
.modal-close-button {
  position: absolute;
  top: 10px;
  right: 20px;
  font-size: 1.5rem;
  width: fit-content;
  padding: 1em;
  display: flex;
  align-content: center;
  background-color: transparent;
  i {
    color: white;
  }
}

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
  ul {
    display: flex;
    justify-content: center;
    li {
      text-align: center;
      margin-top: 50px;
      list-style-type: none;
      width: 130px;
    }
  }
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

@media screen and (min-width: 1200px) {
  #logo {
    width: 30%;
  }
}

@media screen and (min-width: 1400px) {
  #logo {
    width: 40%;
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
