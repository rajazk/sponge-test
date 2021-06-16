<template>
  <div id="app">
    <div class="top-logo">
      <img src="./assets/sponge-logo.svg" alt="no image" />
    </div>
    <div class="Slick-crousal-wrapper">
      <VueSlickCarousel v-bind="settings">
        <div class="slick-slide">
          <img src="./assets/1.jpg" alt="" />
        </div>
        <div class="slick-slide">
          <img src="./assets/2.jpg" alt="" />
        </div>
        <div class="slick-slide">
          <img src="./assets/3.jpg" alt="" />
        </div>
        <div class="slick-slide">
          <img src="./assets/4.jpg" alt="" />
        </div>
        <div class="slick-slide">
          <img src="./assets/5.jpg" alt="" />
        </div>
        <div class="slick-slide">
          <img src="./assets/6.jpg" alt="" />
        </div>
        <div class="slick-slide">
          <img src="./assets/7.jpg" alt="" />
        </div>
      </VueSlickCarousel>
    </div>
    <div class="form-wrapper">
      <div class="form-container">
        <form>
          <div class="row">
            <div class="col-md-6">
              <div class="form-group">
                <label for="exampleInputPassword1">Name</label>
                <input
                  v-model="name"
                  type="text"
                  class="form-control"
                  id="exampleInputPassword1"
                  placeholder="Enter Your Name"
                />
              </div>
            </div>
            <div class="col-md-6">
              <div class="form-group">
                <label for="exampleInputEmail1">Email address</label>
                <input
                  v-model="email"
                  type="email"
                  class="form-control"
                  id="exampleInputEmail1"
                  aria-describedby="emailHelp"
                  placeholder="Enter Your Email"
                />
                <small id="emailHelp" class="form-text text-muted"
                  >We'll never share your email with anyone else.</small
                >
              </div>
            </div>

            <div class="col-md-12">
              <div class="form-group">
                <label for="exampleInputPassword1">Message</label>
                <textarea
                  v-model="message"
                  class="form-control"
                  id="exampleInputPassword1"
                  placeholder=""
                  rows="7"
                ></textarea>
              </div>
            </div>
          </div>
          <button type="button" class="btn btn-primary" v-on:click="greet">
            Submit
          </button>
        </form>
      </div>
    </div>
    <div class="footer-wrapper">
      <div class="row">
        <div class="peacock col-lg-3 col-md-6 col-sm-12">
          <img src="./assets/5.jpg" alt="" />
          <h2>Peacock</h2>
          <p>
            Peacocks, also known as peafowl, are medium sized birds most closely
            related to pheasants. Peacocks inhabit warm climates of the Southern
            Hemisphere. All peacocks are believed to have originated in Asia,
            but they now inhabit Africa and parts of Australia.
          </p>
        </div>
        <div class="peacock col-lg-3 col-md-6 col-sm-12">
          <img src="./assets/5.jpg" alt="" />
          <h2>Peacock</h2>
          <p>
            Peacocks, also known as peafowl, are medium sized birds most closely
            related to pheasants. Peacocks inhabit warm climates of the Southern
            Hemisphere. All peacocks are believed to have originated in Asia,
            but they now inhabit Africa and parts of Australia.
          </p>
        </div>
        <div class="peacock col-lg-3 col-md-6 col-sm-12">
          <img src="./assets/5.jpg" alt="" />
          <h2>Peacock</h2>
          <p>
            Peacocks, also known as peafowl, are medium sized birds most closely
            related to pheasants. Peacocks inhabit warm climates of the Southern
            Hemisphere. All peacocks are believed to have originated in Asia,
            but they now inhabit Africa and parts of Australia.
          </p>
        </div>
        <div class="peacock col-lg-3 col-md-6 col-sm-12">
          <img src="./assets/5.jpg" alt="" />
          <h2>Peacock</h2>
          <p>
            Peacocks, also known as peafowl, are medium sized birds most closely
            related to pheasants. Peacocks inhabit warm climates of the Southern
            Hemisphere. All peacocks are believed to have originated in Asia,
            but they now inhabit Africa and parts of Australia.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
import "./assets/css/style.css";
export default {
  name: "App",
  components: {
    VueSlickCarousel,
  },
  data() {
    return {
      name: "",
      email: "",
      message: "",
      settings: {
        dots: true,
        infinite: true,
        slidesToScroll: 1,
        slidesToShow: 4,
        adaptiveHeight: true,
        autoplay: true,
        autoplaySpeed: 10000,
        responsive: [
          {
            breakpoint: 1441,
            settings: {
              slidesToShow: 4,
              slidesToScroll: 3,
              infinite: true,
              dots: true,
            },
          },
          {
            breakpoint: 1260,
            settings: {
              slidesToShow: 3,
              slidesToScroll: 2,
            },
          },
          {
            breakpoint: 981,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 1,
            },
          },
          {
            breakpoint: 699,
            settings: {
              slidesToShow: 1,
              slidesToScroll: 1,
            },
          },
        ],
      },
    };
  },
  methods: {
    greet() {
      alert(
        `Details are: Name: ${this.name} Email ${this.email} MEssage: ${this.message}`
      );
    },
  },
};
</script>

<style>
@import "~bootstrap/dist/css/bootstrap.css";
</style>
