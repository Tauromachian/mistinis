<template>
  <section id="section-races-carousel" class="section-races-carousel">
    <div class="tab">
      <a
        id="tab-button-halfingai"
        class="tablinks active"
        @click="(event) => openCity(event, 'tab-halfingai')"
      >
        Halfingai
      </a>
      <span>|</span>
      <a
        id="tab-button-uritonai"
        class="tablinks"
        @click="(event) => openCity(event, 'tab-uritonai')"
      >
        Uritonai
      </a>
      <span>|</span>
      <a
        id="tab-button-tabaksiai"
        class="tablinks"
        @click="(event) => openCity(event, 'tab-tabaksiai')"
      >
        Tabaksiai
      </a>
      <span>|</span>
      <a
        id="tab-button-minotaurai"
        class="tablinks"
        @click="(event) => openCity(event, 'tab-minotaurai')"
      >
        Minotaurai
      </a>
    </div>
    <div id="tab-halfingai" class="tabcontent">
      <img src="images/rases_img/Haflingas.png" alt="" />
      <div class="tabcontent-content container">
        <div class="tab-description">
          <h2>Halfingai</h2>
          <p>
            Haflingai yra draugiškiausia bendruomenė su kuriais galite
            susidurti, kilę iš sausos žinduolių. Jie yra nerūpestingi, drąsus ir
            darbštūs, dauguma jų patenkinti savo gyvenimu, kupinu paprastų
            malonumų. Bendrame rasių tarpe jie gerai žinomi ne tik dėl savo
            geranoriškumo ir draugiškumo, o taip pat gerai atpažįstami dėl savo
            žemo ūgio. Kol jie turės puikią kompaniją ir laisvę siekti savo
            svajonių, Haflingas bus laimingas. Haflingai labiausiai vertina
            dvasines vertybes ir yra naiviai geri, ši savybė dažnai jiems ne į
            naudą, tačiau jie turi daugumą privalumų, vieni iš jų- puikus
            sugebėjimas vystyti pramonę ir savo kraštų aprūpinimą žaliavomis ir
            greitas jų transportavimas, nes Haflingai greičiausi iš visų
            Mistinio pasaulio rasių. Haflingų šūkis: -Ūgis neturi reikšmės,
            reikšmė - valioje!
          </p>
        </div>
      </div>
    </div>
    <div id="tab-uritonai" class="tabcontent">
      <img src="images/rases_img/Uritonas.png" alt="" />
      <div class="tabcontent-content container">
        <div class="tab-description">
          <h2>Uritonai</h2>
          <p>
            Uritonai yra iš vandens bakterijų išsivystę humanoidai, kurių
            organizmas ir kūnas prisitaikęs prie povandeninio gyvenimo sąlygų,
            mėlyna oda ir spalvingi plaukai Uritonų išskirtinis bruožas tarp
            rasių. Jie yra ne tik vandenyno gelmių, bet, jei jų paklaustumėte,
            viso pasaulio gynėjai. Nors yra tam tikra arogancija, kurios
            didžioji dalis kyla iš tokio izoliuoto gyvenimo, jie tikrai saugo
            tuos, kuriems reikia pagalbos. Tai reiškia, kad jų arogantiškas ir
            kartais per daug sąžiningas, teisingas, visas taisykles atitinkantis
            elgesys kai kuriuos gali atgrasinti, tačiau Uritonams tai priimtina
            ir nepaisant to, jie pasiruošę padėti visiems sunkioje situacijoje,
            jie neatstumia kitų. Uritonai tiesiog nėra pripratę prie gyvenimo
            kuris vyksta už jų giliavandenių namų ribų. Dėl tokios Uritonų rasės
            ypatybės jie gali kvėpuoti po vandeniu ir matyti gilioje tamsoje tai
            jiems leidžia gyventi savo atskirame vandens pasaulyje. Uritonų
            šūkis: -Nespręsk apie knygą, iš jos viršelio. Arba, -Atsiminus savo
            blogumą, žiūrėk į kitų gerumą.
          </p>
        </div>
      </div>
    </div>
    <div id="tab-tabaksiai" class="tabcontent">
      <img src="images/rases_img/Tabaksis.png" alt="" />
      <div class="tabcontent-content container">
        <div class="tab-description">
          <h2>Tabaksiai</h2>
          <p>
            Tabaksiai yra iš žinduolių-kačių išsivystę humanoidai, kurių
            smalsumas toks pat stiprus kaip ir tikrosios katės, tačiau jų dar
            vienas privalumas - aukštas intelektas. Tabaksiai nukeliaus
            neįtikėtinai toli, jei jų troškimas nukeliauti. Jie be galo
            užsispyrę ir savo tikslų laikosi. Tabaksiai linkę laikytis savo
            tradicijų ir nuomonės, jog protiniai sugebėjimai yra progreso
            variklis, jie nelinkę kariauti ir užkariauti kitų kraštų be
            priežasties, viskas stengiamasi išspręsti diplomatijos pagalba, dėl
            to jiems dažniausiai nusišypso sėkmė. Tabaksių šūkis: -Gyvenime
            reikia tik tiek aukso, kad išgyventum, bet kas daugiau, yra laikoma
            nereikalinga našta.
          </p>
        </div>
      </div>
    </div>
    <div id="tab-minotaurai" class="tabcontent">
      <img src="images/rases_img/Minotauras.png" alt="" />
      <div class="tabcontent-content container">
        <div class="tab-description">
          <h2>Minotaurai</h2>
          <p>
            Minotaurai yra į galingus stumbrus panašūs humanoidai, turintys
            stiprų agresijos potraukį ir tvirtą sąžinę. Šie du, iš pirmo
            žvilgsnio prieštaraujantys aspektai reiškia, kad Minotauras yra
            karinga asmenybė, linkusi bent kokia kaina ginti savo teritoriją. Ne
            visi Minotaurai sugeba atsispirti savo smarkesnių potraukių
            pagundai, tačiau tie, kurie puikiai susivaldo, yra gerbiami, o tai
            atsispindi jų visuomenėje ir kasdieniame gyvenime. Įgūdžių
            tobulinimas ir technikų įvaldymas teikia Minotaurams didelį malonumą
            ir galbūt yra vienas iš svarbiausių dalykų, padedančių atsispirti
            kitiems potraukiams. Minotaurai labiausiai agresyvūs rasių tarpe,
            dėl to kitos rasės be reikalo su jais nejuokauja, taip pat dėl tokio
            gyvenimo būdo jie yra stipriausi ir ištvermingiausi iš rasių, dėl to
            linkę viską gauti jėga. Minotaurų šūkis: -Kas turi jėgą, tas ir
            tiesą - kieno galia, to ir valia.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import debounce from 'basic-debouncer'

export default {
  name: 'SectionRacesCarousel',
  mounted() {
    this.initTouchAction()
  },
  methods: {
    initTouchAction() {
      const section = document.getElementById('section-races-carousel')
      const tabsIds = [
        'tab-button-halfingai',
        'tab-button-uritonai',
        'tab-button-tabaksiai',
        'tab-button-minotaurai',
      ]

      let startx // starting x coordinate of touch point
      let dist = 0 // distance traveled by touch point
      let touchobj = null // Touch object holder

      section.addEventListener(
        'touchstart',
        function (e) {
          touchobj = e.changedTouches[0] // reference first touch point
          startx = parseInt(touchobj.clientX) // get x coord of touch point
        },
        false
      )

      section.addEventListener(
        'touchmove',
        (e) =>
          debounce(() => {
            touchobj = e.changedTouches[0] // reference first touch point for this event
            dist = parseInt(touchobj.clientX) - startx // calculate dist traveled by touch point
            // move box according to starting pos plus dist
            // with lower limit 0 and upper limit 380 so it doesn't move outside track:
            if (dist < -20) {
              this.slideRight(tabsIds)
            } else {
              this.slideLeft(tabsIds)
            }
          }),
        false
      )
    },
    slideLeft(tabsIds) {
      const index = this.getIndexOfNextTabToActivate(tabsIds, 'left')
      document.getElementById(tabsIds[index]).click()
    },
    slideRight(tabsIds) {
      const index = this.getIndexOfNextTabToActivate(tabsIds, 'right')
      document.getElementById(tabsIds[index]).click()
    },
    getIndexOfNextTabToActivate(tabs, direction) {
      const index = this.getIndexOfActiveTab(tabs)
      if (direction === 'right') {
        return this.getIndexOfRightTab(index, tabs.length - 1)
      } else {
        return this.getIndexOfLeftTab(index, tabs.length - 1)
      }
    },
    getIndexOfRightTab(index, length) {
      if (index === length) return 0
      return ++index
    },
    getIndexOfLeftTab(index, length) {
      if (index === 0) return length
      return --index
    },
    getIndexOfActiveTab(tabs) {
      const tab = tabs.find((tab) => {
        const tabTag = document.getElementById(tab)
        return tabTag.classList.contains('active')
      })
      return tabs.indexOf(tab)
    },
    openCity(evt, raceName) {
      let i
      const tabcontent = document.getElementsByClassName('tabcontent')
      for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = 'none'
      }
      const tablinks = document.getElementsByClassName('tablinks')
      for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(' active', '')
      }
      document.getElementById(raceName).style.display = 'block'
      evt.currentTarget.className += ' active'
    },
  },
}
</script>

<style lang="scss" scoped>
.section-races-carousel {
  overflow: hidden;
  position: relative;
  height: fit-content;
  padding: 0 5px;
  .tab {
    position: absolute;
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    justify-content: center;
    gap: 10px;
    cursor: pointer;
    top: 70px;
    z-index: 100;

    @media screen and (min-width: 800px) {
      gap: 20px;
    }

    @media screen and (min-width: 1500px) {
      gap: 30px;
    }
  }
  /* Create an active/current tablink class */
  .tab a.active {
    color: #ad00ff;
  }

  /* Style the tab content */
  .tabcontent {
    display: none;
    padding: 6px 12px;
    border-top: none;
    width: 100%;

    img {
      position: absolute;
      flex-basis: 50%;
      height: 100%;
      width: auto;
      z-index: 10;
    }

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

  .tabcontent-content {
    z-index: 30;
    position: relative;
    display: flex;

    .tab-description {
      position: relative;
      flex-basis: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      margin-left: auto;
      padding-top: 8em;
      padding-bottom: 5em;
    }

    @media screen and (min-width: 800px) {
      .tab-description {
        flex-basis: 60%;
        padding-top: 10em;
        padding-bottom: 10em;
      }
    }

    @media screen and (min-width: 1500px) {
      .tab-description {
        padding-top: 20em;
        padding-bottom: 20em;
      }
    }
  }

  #tab-halfingai,
  #tab-uritonai,
  #tab-tabaksiai,
  #tab-minotaurai {
    padding: 0;
  }

  #tab-halfingai {
    display: block;
    background-image: url('/images/rases_img/Haflingai_bg.png');
    background-repeat: no-repeat;
    background-size: cover;
  }

  #tab-halfingai h2 {
    color: #05ff00;
  }

  #tab-uritonai {
    background-image: url('/images/rases_img/Uritonai_bg.png');
    background-repeat: no-repeat;
    background-size: cover;
  }

  #tab-uritonai h2 {
    color: #0038ff;
  }

  #tab-tabaksiai {
    background-image: url('/images/rases_img/Tabaksiai_bg.png');
    background-repeat: no-repeat;
    background-size: cover;
  }

  #tab-tabaksiai h2 {
    color: #ffe600;
  }

  #tab-minotaurai {
    background-image: url('/images/rases_img/Minotaurai_bg.png');
    background-repeat: no-repeat;
    background-size: cover;
  }

  #tab-minotaurai h2 {
    color: #ff0000;
  }
}
</style>
