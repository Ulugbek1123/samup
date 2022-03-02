<template>
  <section class="portfolio" id="portfolio">
    <v-container fluid>
      <v-row class="d-none__sm">
        <v-col cols="12" md="2">
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 53.jpg')"
            alt=""
          />
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 54.jpg')"
            alt=""
          />
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 55.jpg')"
            alt=""
          />
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 56.jpg')"
            alt=""
          />
        </v-col>
        <v-col cols="12" md="8">
          <v-row style="height: 100%;">
            <v-col cols="12">
              <v-row>
                <v-col
                  cols="12"
                  sm="7"
                  class="ma-auto d-flex justify-center align-center flex-column"
                >
                  <h3>Zamonaviy upakovkaga buyurtma bering!</h3>
                  <p>
                    Biz bilan bog’laning va o'z mahsulotingiz uchun chiroyli,
                    zamonaviy dizayn va upakovkaga ega bo'ling.
                  </p>
                  <v-btn class="btnDep" tag="a" target="_blank" href="https://t.me/SamUpDesign" depressed color="#FEB11B">
                    Buyurtma berish
                  </v-btn>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="6" sm="4" class="d-flex justify-center flex-column">
              <img :src="require('../assets/img/Group 57.jpg')" alt="" />
              <img :src="require('../assets/img/Group 58.jpg')" alt="" />
              <img :src="require('../assets/img/Group 59.jpg')" alt="" />
              <img
                :src="require('../assets/img/Group 55.jpg')"
                class="d-none_sm"
                alt=""
              />
              <img
                :src="require('../assets/img/Group 56.jpg')"
                class="d-none_sm"
                alt=""
              />
            </v-col>
            <v-col
              cols="6"
              sm="4"
              class="d-flex justify-end flex-column"
              style="transform:translateY(100px);"
            >
              <img :src="require('../assets/img/Group 60.jpg')" alt="" />
              <img :src="require('../assets/img/Group 61.jpg')" alt="" />
              <img :src="require('../assets/img/Group 62.jpg')" alt="" />
              <img
                :src="require('../assets/img/Group 68.jpg')"
                class="d-none_sm"
                alt=""
              />
              <img
                :src="require('../assets/img/Group 69.jpg')"
                class="d-none_sm"
                alt=""
              />
            </v-col>
            <v-col cols="6" sm="4" class="d-flex justify-center flex-column">
              <img
                :src="require('../assets/img/Group 63.jpg')"
                class="d-none_xs"
              />
              <img
                :src="require('../assets/img/Group 64.jpg')"
                class="d-none_xs"
              />
              <img
                :src="require('../assets/img/Group 65.jpg')"
                class="d-none_xs "
              />
              <img
                :src="require('../assets/img/Group 66.jpg')"
                class="d-none_xs d-none_sm"
                alt=""
              />
              <img
                :src="require('../assets/img/Group 67.jpg')"
                class="d-none_xs d-none_sm"
                alt=""
              />
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" md="2">
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 66.jpg')"
            alt=""
          />
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 67.jpg')"
            alt=""
          />
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 68.jpg')"
            alt=""
          />
          <img
            class="d-block-sm"
            :src="require('../assets/img/Group 69.jpg')"
            alt=""
          />
        </v-col>
      </v-row>
      <v-row class="d-block__sm">
        <v-col
          cols="12"
          sm="7"
          class="ma-auto d-flex justify-center align-center flex-column"
        >
          <h3>Zamonaviy upakovkaga buyurtma bering!</h3>
          <p>
            Biz bilan bog’laning va o'z mahsulotingiz uchun chiroyli, zamonaviy
            dizayn va upakovkaga ega bo'ling.
          </p>
          <v-btn class="btnDep" tag="a" depressed color="#FEB11B">
            Buyurtma berish
          </v-btn>
        </v-col>
      </v-row>
      <swiper class="swiper d-block__sm" :options="swiperOption">
        <swiper-slide
          class="d-flex flex-column justify-center"
          v-for="n in clients"
          :key="n"
        >
          <img :src="l.img" v-for="l in n.one" :key="l" alt="" />
        </swiper-slide>
      </swiper>
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
            img: require("../assets/img/Group 53.jpg"),
          },
          {
            img: require("../assets/img/Group 54.jpg"),
          },
          {
            img: require("../assets/img/Group 55.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/img/Group 56.jpg"),
          },
          {
            img: require("../assets/img/Group 57.jpg"),
          },
          {
            img: require("../assets/img/Group 58.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/img/Group 59.jpg"),
          },
          {
            img: require("../assets/img/Group 60.jpg"),
          },
          {
            img: require("../assets/img/Group 61.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/img/Group 62.jpg"),
          },
          {
            img: require("../assets/img/Group 63.jpg"),
          },
          {
            img: require("../assets/img/Group 64.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/img/Group 65.jpg"),
          },
          {
            img: require("../assets/img/Group 66.jpg"),
          },
          {
            img: require("../assets/img/Group 67.jpg"),
          },
        ],
      },
      {
        one: [
          {
            img: require("../assets/img/Group 68.jpg"),
          },
          {
            img: require("../assets/img/Group 69.jpg"),
          },
          {
            img: require("../assets/img/Group 63.jpg"),
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
<style lang="scss" scoped>
section {
  padding-top: 100px;
  padding-bottom: 250px;
}
img {
  max-width: 100%;
  height: auto;
  padding: 15px 0;
}
h3 {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 130%;
  text-align: center;
  color: #000000;
  padding: 0 52px;
}
p {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 24px;
  line-height: 130%;
  text-align: center;
  color: #000000;
  padding: 0 10px;
  margin-bottom: 30px;
}
.btnDep {
  padding: 23px 62px !important;
  height: auto !important;
  font-weight: 600 !important;
  font-size: 24px !important;
}
.d-none_sm {
  display: none;
}
.d-block__sm {
  display: none;
}
@media (max-width: 1500px) {
  h3 {
    font-family: "Open Sans";
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 130%;
    text-align: center;
    color: #000000;
    padding: 0 52px;
  }
  p {
    font-family: "Open Sans";
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 130%;
    text-align: center;
    color: #000000;
    padding: 0 10px;
    margin-bottom: 30px;
  }
  .btnDep {
    padding: 23px 62px !important;
    height: auto !important;
    font-weight: 600 !important;
    font-size: 18px !important;
  }
}
@media (max-width: 959px) {
  section {
    padding-top: 60px;
    padding-bottom: 100px;
  }
  .d-none_sm {
    display: block;
  }
  .d-block-sm {
    display: none;
  }
  h3 {
    font-family: "Open Sans";
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 130%;
    text-align: center;
    color: #000000;
    padding: 0 52px;
  }
  p {
    font-family: "Open Sans";
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 130%;
    text-align: center;
    color: #000000;
    padding: 0 10px;
    margin-bottom: 30px;
  }
  .btnDep {
    padding: 23px 62px !important;
    height: auto !important;
    font-weight: 600 !important;
    font-size: 24px !important;
  }
}
@media (max-width: 599px) {
  .d-none_xs {
    display: none;
  }
}
@media (max-width: 599px) {
  .btnDep {
    padding: 20px 30px !important;
    height: auto !important;
    font-weight: 600 !important;
    font-size: 20px !important;
  }
  .d-none__sm {
    display: none;
  }
  .d-block__sm {
    display: block;
  }
}
</style>
