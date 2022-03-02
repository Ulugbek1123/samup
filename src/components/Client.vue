<template>
  <section id="client">
    <h2>Mijozlarimiz</h2>
    <v-container>
      <v-row>
        <swiper :options="swiperOption">
          <swiper-slide
            class="d-flex flex-column justify-center"
            v-for="n in clients"
            :key="n"
          >
            <img :src="l.img" v-for="l in n.one" :key="l" alt="" />
          </swiper-slide>
        </swiper>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import SwiperCore, { Autoplay } from "swiper";
SwiperCore.use([Autoplay]);
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/swiper-bundle.min.css";
export default {
  data: () => ({
    swiperOption: {
      grabCursor: true,
      loop: true,
      slidesPerView: 5,
      spaceBetween: 10,
      autoplay: {
        enabled: true,
        delay: 2000,
      },
      breakpoints: {
        320: {
          slidesPerView: 2,
          spaceBetween: 20,
        },
        640: {
          slidesPerView: 2,
          spaceBetween: 20,
        },
        768: {
          slidesPerView: 4,
          spaceBetween: 40,
        },
        1024: {
          slidesPerView: 5,
          spaceBetween: 50,
        },
      },
    },
    clients: [
      {
        one: [
          {
            img: require("../assets/client/Group 78.jpg"),
          },
          {
            img: require("../assets/client/Group 79.jpg"),
          },
          {
            img: require("../assets/client/Group 80.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 81.jpg"),
          },
          {
            img: require("../assets/client/Group 82.jpg"),
          },
          {
            img: require("../assets/client/Group 83.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 84.jpg"),
          },
          {
            img: require("../assets/client/Group 85.jpg"),
          },
          {
            img: require("../assets/client/Group 86.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 87.jpg"),
          },
          {
            img: require("../assets/client/Group 88.jpg"),
          },
          {
            img: require("../assets/client/Group 89.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 90.jpg"),
          },
          {
            img: require("../assets/client/Group 91.jpg"),
          },
          {
            img: require("../assets/client/Group 92.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 93.jpg"),
          },
          {
            img: require("../assets/client/Group 94.jpg"),
          },
          {
            img: require("../assets/client/Group 95.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 96.jpg"),
          },
          {
            img: require("../assets/client/Group 97.jpg"),
          },
          {
            img: require("../assets/client/Group 98.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/client/Group 99.jpg"),
          },
          {
            img: require("../assets/client/Group 100.jpg"),
          },
          {
            img: require("../assets/client/Group 85.jpg"),
          },
        ],
      },
    ],
  }),
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>
<style lang="scss">
section#client {
  padding-top: 60px;
  padding-bottom: 100px;
  background: linear-gradient(85.61deg, #ffd176 -4.18%, #fff3b3 100%);
  h2 {
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 42px;
    text-align: center;
    color: #000000;
  }
  .swiper-wrapper {
    img {
      max-width: 100%;
      height: auto;
      margin: 15px 0;
    }
  }
}
</style>
