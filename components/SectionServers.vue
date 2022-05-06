<template>
  <section id="section-servers" class="servers">
    <div class="title-container">
      <h1>Vaizdai iš serverio</h1>
    </div>

    <div class="slider-container">
      <div class="slider-content">
        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/973/200/300"
            alt="1"
          />
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/974/200/300"
            alt="2"
          />
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/975/200/300"
            alt="3"
          />
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/976/200/300"
            alt="4"
          />
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/977/200/300"
            alt="5"
          />
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/978/200/300"
            alt="6"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionServers',
  mounted() {
    const noArrows = false

    const container = document.querySelector('.slider-container')
    const slide = document.querySelectorAll('.slider-single')
    const slideTotal = slide.length - 1
    let slideCurrent = -1

    function initArrows() {
      if (noArrows) {
        return
      }
      const leftArrow = document.createElement('a')
      const iLeft = document.createElement('i')
      iLeft.classList.add('fa')
      iLeft.classList.add('fa-angle-left')
      leftArrow.classList.add('slider-left')
      leftArrow.appendChild(iLeft)
      leftArrow.addEventListener('click', () => {
        slideLeft()
      })
      const rightArrow = document.createElement('a')
      const iRight = document.createElement('i')
      iRight.classList.add('fa')
      iRight.classList.add('fa-angle-right')
      rightArrow.classList.add('slider-right')
      rightArrow.appendChild(iRight)
      rightArrow.addEventListener('click', () => {
        slideRight()
      })
      container.appendChild(leftArrow)
      container.appendChild(rightArrow)
    }

    function slideInitial() {
      initArrows()
      setTimeout(function () {
        slideRight()
      }, 500)
    }

    let preactiveSlide
    let proactiveSlide

    function slideRight() {
      if (slideCurrent < slideTotal) {
        slideCurrent++
      } else {
        slideCurrent = 0
      }

      if (slideCurrent > 0) {
        preactiveSlide = slide[slideCurrent - 1]
      } else {
        preactiveSlide = slide[slideTotal]
      }
      const activeSlide = slide[slideCurrent]
      if (slideCurrent < slideTotal) {
        proactiveSlide = slide[slideCurrent + 1]
      } else {
        proactiveSlide = slide[0]
      }

      slide.forEach((elem) => {
        const thisSlide = elem
        if (thisSlide.classList.contains('preactivede')) {
          thisSlide.classList.remove('preactivede')
          thisSlide.classList.remove('preactive')
          thisSlide.classList.remove('active')
          thisSlide.classList.remove('proactive')
          thisSlide.classList.add('proactivede')
        }
        if (thisSlide.classList.contains('preactive')) {
          thisSlide.classList.remove('preactive')
          thisSlide.classList.remove('active')
          thisSlide.classList.remove('proactive')
          thisSlide.classList.remove('proactivede')
          thisSlide.classList.add('preactivede')
        }
      })
      preactiveSlide.classList.remove('preactivede')
      preactiveSlide.classList.remove('active')
      preactiveSlide.classList.remove('proactive')
      preactiveSlide.classList.remove('proactivede')
      preactiveSlide.classList.add('preactive')

      activeSlide.classList.remove('preactivede')
      activeSlide.classList.remove('preactive')
      activeSlide.classList.remove('proactive')
      activeSlide.classList.remove('proactivede')
      activeSlide.classList.add('active')

      proactiveSlide.classList.remove('preactivede')
      proactiveSlide.classList.remove('preactive')
      proactiveSlide.classList.remove('active')
      proactiveSlide.classList.remove('proactivede')
      proactiveSlide.classList.add('proactive')
    }

    function slideLeft() {
      if (slideCurrent > 0) {
        slideCurrent--
      } else {
        slideCurrent = slideTotal
      }

      if (slideCurrent < slideTotal) {
        proactiveSlide = slide[slideCurrent + 1]
      } else {
        proactiveSlide = slide[0]
      }
      const activeSlide = slide[slideCurrent]
      if (slideCurrent > 0) {
        preactiveSlide = slide[slideCurrent - 1]
      } else {
        preactiveSlide = slide[slideTotal]
      }
      slide.forEach((elem) => {
        const thisSlide = elem
        if (thisSlide.classList.contains('proactive')) {
          thisSlide.classList.remove('preactivede')
          thisSlide.classList.remove('preactive')
          thisSlide.classList.remove('active')
          thisSlide.classList.remove('proactive')
          thisSlide.classList.add('proactivede')
        }
        if (thisSlide.classList.contains('proactivede')) {
          thisSlide.classList.remove('preactive')
          thisSlide.classList.remove('active')
          thisSlide.classList.remove('proactive')
          thisSlide.classList.remove('proactivede')
          thisSlide.classList.add('preactivede')
        }
      })

      preactiveSlide.classList.remove('preactivede')
      preactiveSlide.classList.remove('active')
      preactiveSlide.classList.remove('proactive')
      preactiveSlide.classList.remove('proactivede')
      preactiveSlide.classList.add('preactive')

      activeSlide.classList.remove('preactivede')
      activeSlide.classList.remove('preactive')
      activeSlide.classList.remove('proactive')
      activeSlide.classList.remove('proactivede')
      activeSlide.classList.add('active')

      proactiveSlide.classList.remove('preactivede')
      proactiveSlide.classList.remove('preactive')
      proactiveSlide.classList.remove('active')
      proactiveSlide.classList.remove('proactivede')
      proactiveSlide.classList.add('proactive')
    }

    slideInitial()
  },
}
</script>

<style lang="scss">
$time: 500ms;
$delay: calc($time/2);
$mode: cubic-bezier(0.17, 0.67, 0.55, 1.43);

.slider-container {
  position: relative;
  margin: 0 auto;
  width: 340px;
  height: 300px;

  @media screen and (min-width: 800px) {
    width: 600px;
    height: 400px;
  }

  @media screen and (min-width: 1000px) {
    width: 800px;
    height: 600px;
  }

  @media screen and (min-width: 1200px) {
    width: 1000px;
    height: 800px;
  }

  @media screen and (min-width: 1400px) {
    width: 1200px;
    height: 1000px;
  }

  .slider-content {
    position: relative;
    left: 50%;
    top: 50%;
    width: 70%;
    height: 60%;
    transform: translate(-50%, -50%);
    .slider-single {
      position: absolute;
      z-index: 0;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      transition: z-index 0ms $delay;
      .slider-single-image {
        position: relative;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.2);
        transition: $time $mode;
        transform: scale(0);
        opacity: 0;
      }

      &.preactivede {
        //z-index: 0;
        .slider-single-image {
          //opacity: 0;
          transform: translateX(-50%) scale(0);
        }
      }

      @media screen and (min-width: 800px) {
        &.preactive {
          z-index: 1;
          .slider-single-image {
            opacity: 0.3;
            transform: translateX(-25%) scale(0.8);
          }
        }
      }

      @media screen and (min-width: 800px) {
        &.proactive {
          z-index: 1;
          .slider-single-image {
            opacity: 0.3;
            transform: translateX(25%) scale(0.8);
          }
        }
      }

      &.proactivede {
        //z-index: 0;
        .slider-single-image {
          //opacity: 0;
          transform: translateX(50%) scale(0);
        }
      }
      &.active {
        z-index: 2;
        .slider-single-image {
          opacity: 1;
          transform: translateX(0%) scale(1);
        }
      }
    }
  }
  .slider-left {
    position: absolute;
    z-index: 3;
    display: block;
    right: 85%;
    top: 50%;
    color: #ffffff;
    transform: translateY(-50%);
    padding: 20px 15px;
    margin-right: -2px;
  }
  .slider-right {
    position: absolute;
    z-index: 3;
    display: block;
    left: 85%;
    top: 50%;
    color: #ffffff;
    transform: translateY(-50%);
    padding: 20px 15px;
    margin-left: -2px;
  }
  .not-visible {
    display: none !important;
  }
}

.title-container {
  display: flex;
  justify-content: center;
}
</style>
