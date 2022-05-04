<template>
  <section class="servers">
    <div class="servers__title-container">
      <h2>Vaizdai iš serverio</h2>
    </div>
    <div class="slider-container">
      <div class="slider-content">
        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/973/200/300"
            alt="1"
          />
          <h1 class="slider-single-title">Through the Mountains</h1>
          <a class="slider-single-likes" href="javascript:void(0);">
            <i class="fa fa-heart"></i>
            <p>1,247</p>
          </a>
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/974/200/300"
            alt="2"
          />
          <h1 class="slider-single-title">Through the Mountains</h1>
          <a class="slider-single-likes" href="javascript:void(0);">
            <i class="fa fa-heart"></i>
            <p>1,247</p>
          </a>
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/975/200/300"
            alt="3"
          />
          <h1 class="slider-single-title">Through the Mountains</h1>
          <a class="slider-single-likes" href="javascript:void(0);">
            <i class="fa fa-heart"></i>
            <p>1,247</p>
          </a>
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/976/200/300"
            alt="4"
          />
          <h1 class="slider-single-title">Through the Mountains</h1>
          <a class="slider-single-likes" href="javascript:void(0);">
            <i class="fa fa-heart"></i>
            <p>1,247</p>
          </a>
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/977/200/300"
            alt="5"
          />
          <h1 class="slider-single-title">Through the Mountains</h1>
          <a class="slider-single-likes" href="javascript:void(0);">
            <i class="fa fa-heart"></i>
            <p>1,247</p>
          </a>
        </div>

        <div class="slider-single">
          <img
            class="slider-single-image"
            src="https://picsum.photos/id/978/200/300"
            alt="6"
          />
          <h1 class="slider-single-title">Through the Mountains</h1>
          <a class="slider-single-likes" href="javascript:void(0);">
            <i class="fa fa-heart"></i>
            <p>1,247</p>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionServers',
}
</script>

<style lang="scss">
.slider-container {
  position: relative;
  margin: 0 auto;
  width: 800px;
  height: 600px;
}

.slider-container .bullet-container {
  position: absolute;
  bottom: 10px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slider-container .bullet-container .bullet {
  margin-right: 14px;

  height: 20px;
  width: 20px;
  border-radius: 50%;
  background-color: white;
  opacity: 0.5;
}

.slider-container .bullet-container .bullet:last-child {
  margin-right: 0px;
}

.slider-container .slider-content {
  position: relative;
  left: 50%;
  top: 50%;
  width: 70%;
  height: 60%;
  transform: translate(-50%, -50%);
}

.slider-container .slider-content .slider-single {
  position: absolute;
  z-index: 0;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  transition: z-index 0ms 1;
}

.slider-container .slider-content .slider-single .slider-single-image {
  position: relative;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.2);
  transition: 1 cubic-bezier(0.17, 0.67, 0.55, 1.43);
  transform: scale(0);
  opacity: 0;
}

.slider-container .slider-content .slider-single .slider-single-download {
  position: absolute;
  display: block;
  right: -22px;
  bottom: 12px;
  padding: 15px;
  color: #333333;
  background-color: #fdc84b;
  font-size: 18px;
  font-weight: 600;
  font-family: 'karla';
  border-radius: 5px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
  transition: 1 cubic-bezier(0.17, 0.67, 0.55, 1.43);
  opacity: 0;
}

.slider-container .slider-content .slider-single .slider-single-download:hover,
:focus {
  outline: none;
  text-decoration: none;
}

.slider-container .slider-content .slider-single .slider-single-title {
  display: block;
  float: left;
  margin: 16px 0 0 20px;
  font-size: 20px;
  font-family: 'karla', sans-serif;
  font-weight: 400;
  color: #ffffff;
  transition: 1 cubic-bezier(0.17, 0.67, 0.55, 1.43);
  opacity: 0;
}

.slider-container
  .slider-content
  .slider-single
  .slider-single-title.preactivede
  .slider-single-image {
  transform: translateX(-50%) scale(0);
}

.slider-container .slider-left {
  position: absolute;
  z-index: 3;
  display: block;
  right: 85%;
  top: 50%;
  color: #ffffff;
  transform: translateY(-50%);
  padding: 20px 15px;
  border-top: 2px solid #fdc84b;
  border-right: 2px solid #fdc84b;
  border-bottom: 2px solid #fdc84b;
  border-left: 2px solid #fdc84b;
  margin-right: -2px;
}

.slider-container .slider-right {
  position: absolute;
  z-index: 3;
  display: block;
  left: 85%;
  top: 50%;
  color: #ffffff;
  transform: translateY(-50%);
  padding: 20px 15px;
  border-top: 2px solid #fdc84b;
  border-right: 2px solid #fdc84b;
  border-bottom: 2px solid #fdc84b;
  border-left: 2px solid #fdc84b;
  margin-left: -2px;
}

.slider-container .not-visible {
  display: none !important;
}
</style>
