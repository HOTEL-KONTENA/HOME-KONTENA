<template>
  <div>
    <div class="top-title">
      <img src="/logo.png" class="img-fluid d-inline-block align-top" alt="" />
    </div>
    <div class="row pt-3 w-100 ml-0 align-item-center footer-title" style="position: absolute; bottom: 0px;">
      <div class="col-6">
        <h6 class="text-white mt-2">HOTELKONTENA.COM</h6>
      </div> 
      <div class="col-6 text-right">
        <p class="text-white small">KH. Agus Salim</p>
      </div>
    </div>
    <b-carousel
      id="carousel-fade"
      style="text-shadow: 0px 0px 2px #000"
      controls
      fade
      indicators
    >
      <b-carousel-slide
        caption="First slide"
        img-src="http://sgp1.digitaloceanspaces.com/basilhotel/kontena/images/images-1.jpg"
      ></b-carousel-slide>
      <b-carousel-slide
        caption="Second Slide"
        img-src="http://sgp1.digitaloceanspaces.com/basilhotel/kontena/images/images-1.jpg"
      ></b-carousel-slide>
      <b-carousel-slide
        caption="Third Slide"
        img-src="http://sgp1.digitaloceanspaces.com/basilhotel/kontena/images/images-3.jpg"
      ></b-carousel-slide>
    </b-carousel>
  </div>

  <!-- <div>
    <div class="container fill">
      <div id="myCarousel" class="carousel slide">
        <div class="carousel-inner">
          <div class="active item">
            <div class="fill" style="background-image:url('//placehold.it/1024x700/449955/FFF');">
              <div class="container">
                
              </div>
            </div>
          </div>
          <div class="item">
            <div class="fill" style="background-image:url('//placehold.it/1024x700');">
              <div class="container">
                
              </div>
            </div>
          </div>
          <div class="item">
            <div class="fill" style="background-image:url('//placehold.it/1024x700/CC1111/FFF');">
              <div class="container">
                
              </div>
            </div>
          </div>
        </div>
        <div class="pull-center">
        <a class="carousel-control left" href="#myCarousel" data-slide="prev">‹</a>
        <a class="carousel-control right" href="#myCarousel" data-slide="next">›</a>
        </div>
      </div>
    </div>
  </div> -->
  <!-- <div class="container">
    <div>
      <logo />
      <h1 class="title">
        Kontena-Website
      </h1>
      <h2 class="subtitle">
        My posh Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div> -->
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
  .top-title {
    position: fixed;
    top: 0;
    left: 3rem;
    width: 7rem;
    padding: 20px;
    height: 5.75rem;
    background-color: #fcfcfc;
    border: 2px solid #000;
    border-top: 0;
    z-index: 999999;
  }
  .footer-title {
    position: absolute;
    background-color: #fcfcfc;
    border: 2px solid #000;
    border-top: 0;
    bottom: 0;
    z-index: 999;
  }
</style>
