<template>
  <section class="container races">
    <div class="tab">
      <a class="tablinks" @click="(event) => openCity(event, 'tab-halfingai')">
        Halfingai
      </a>
      <a class="tablinks" @click="(event) => openCity(event, 'tab-uritonai')">
        Uritonai
      </a>
      <a class="tablinks" @click="(event) => openCity(event, 'tab-tabakisai')">
        Tabaksiai
      </a>
      <a class="tablinks" @click="(event) => openCity(event, 'tab-minotaurai')">
        Minotaurai
      </a>
    </div>
    <div id="tab-halfingai" class="tabcontent">
      <h2>Halfingai</h2>
      <p>
        Haflingai yra draugiškiausia bendruomenė su kuriais galite susidurti,
        kilę iš sausos žinduolių. Jie yra nerūpestingi, drąsus ir darbštūs,
        dauguma jų patenkinti savo gyvenimu, kupinu paprastų malonumų. Bendrame
        rasių tarpe jie gerai žinomi ne tik dėl savo geranoriškumo ir
        draugiškumo, o taip pat gerai atpažįstami dėl savo žemo ūgio. Kol jie
        turės puikią kompaniją ir laisvę siekti savo svajonių, Haflingas bus
        laimingas. Haflingai labiausiai vertina dvasines vertybes ir yra naiviai
        geri, ši savybė dažnai jiems ne į naudą, tačiau jie turi daugumą
        privalumų, vieni iš jų- puikus sugebėjimas vystyti pramonę ir savo
        kraštų aprūpinimą žaliavomis ir greitas jų transportavimas, nes
        Haflingai greičiausi iš visų Mistinio pasaulio rasių. Haflingų šūkis:
        -Ūgis neturi reikšmės, reikšmė - valioje!
      </p>
    </div>
    <div id="tab-uritonai" class="tabcontent">
      <h2>Uritonai</h2>
      <p>
        Uritonai yra iš vandens bakterijų išsivystę humanoidai, kurių organizmas
        ir kūnas prisitaikęs prie povandeninio gyvenimo sąlygų, mėlyna oda ir
        spalvingi plaukai Uritonų išskirtinis bruožas tarp rasių. Jie yra ne tik
        vandenyno gelmių, bet, jei jų paklaustumėte, viso pasaulio gynėjai. Nors
        yra tam tikra arogancija, kurios didžioji dalis kyla iš tokio izoliuoto
        gyvenimo, jie tikrai saugo tuos, kuriems reikia pagalbos. Tai reiškia,
        kad jų arogantiškas ir kartais per daug sąžiningas, teisingas, visas
        taisykles atitinkantis elgesys kai kuriuos gali atgrasinti, tačiau
        Uritonams tai priimtina ir nepaisant to, jie pasiruošę padėti visiems
        sunkioje situacijoje, jie neatstumia kitų. Uritonai tiesiog nėra
        pripratę prie gyvenimo kuris vyksta už jų giliavandenių namų ribų. Dėl
        tokios Uritonų rasės ypatybės jie gali kvėpuoti po vandeniu ir matyti
        gilioje tamsoje tai jiems leidžia gyventi savo atskirame vandens
        pasaulyje. Uritonų šūkis: -Nespręsk apie knygą, iš jos viršelio. Arba,
        -Atsiminus savo blogumą, žiūrėk į kitų gerumą.
      </p>
    </div>
    <div id="tab-tabakisai" class="tabcontent">
      <h2>Tabaksiai</h2>
      <p>
        Tabaksiai yra iš žinduolių-kačių išsivystę humanoidai, kurių smalsumas
        toks pat stiprus kaip ir tikrosios katės, tačiau jų dar vienas
        privalumas - aukštas intelektas. Tabaksiai nukeliaus neįtikėtinai toli,
        jei jų troškimas nukeliauti. Jie be galo užsispyrę ir savo tikslų
        laikosi. Tabaksiai linkę laikytis savo tradicijų ir nuomonės, jog
        protiniai sugebėjimai yra progreso variklis, jie nelinkę kariauti ir
        užkariauti kitų kraštų be priežasties, viskas stengiamasi išspręsti
        diplomatijos pagalba, dėl to jiems dažniausiai nusišypso sėkmė. Tabaksių
        šūkis: -Gyvenime reikia tik tiek aukso, kad išgyventum, bet kas daugiau,
        yra laikoma nereikalinga našta.
      </p>
    </div>
    <div id="tab-minotaurai" class="tabcontent">
      <h2>Minotaurai</h2>
      <p>
        Minotaurai yra į galingus stumbrus panašūs humanoidai, turintys stiprų
        agresijos potraukį ir tvirtą sąžinę. Šie du, iš pirmo žvilgsnio
        prieštaraujantys aspektai reiškia, kad Minotauras yra karinga asmenybė,
        linkusi bent kokia kaina ginti savo teritoriją. Ne visi Minotaurai
        sugeba atsispirti savo smarkesnių potraukių pagundai, tačiau tie, kurie
        puikiai susivaldo, yra gerbiami, o tai atsispindi jų visuomenėje ir
        kasdieniame gyvenime. Įgūdžių tobulinimas ir technikų įvaldymas teikia
        Minotaurams didelį malonumą ir galbūt yra vienas iš svarbiausių dalykų,
        padedančių atsispirti kitiems potraukiams. Minotaurai labiausiai
        agresyvūs rasių tarpe, dėl to kitos rasės be reikalo su jais nejuokauja,
        taip pat dėl tokio gyvenimo būdo jie yra stipriausi ir ištvermingiausi
        iš rasių, dėl to linkę viską gauti jėga. Minotaurų šūkis: -Kas turi
        jėgą, tas ir tiesą - kieno galia, to ir valia.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionRacesCarousel',
  methods: {
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
.tab {
  display: flex;
  width: 100%;
  justify-content: center;
  gap: 30px;
  cursor: pointer;
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
}

#tab-halfingai {
  display: block;
}
</style>
