<template>
  <section class="about" id="services">
    <h1 class="text-center">Bizning xizmatlarimiz</h1>
    <v-container class="container">
      <v-row>
        <v-col v-for="n in cards" :key="n.img" cols="12" sm="6" md="3">
          <v-card elevation="0" class="text-center">
            <img :src="n.img" alt="" />
            <h3 v-html="n.title"></h3>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import img1 from "../assets/logo/1.svg";
import img2 from "../assets/logo/2.svg";
import img3 from "../assets/logo/3.svg";
import img4 from "../assets/logo/4.svg";
import img5 from "../assets/logo/5.svg";
import img6 from "../assets/logo/6.svg";
import img7 from "../assets/logo/7.svg";
import img8 from "../assets/logo/8.svg";
import img from "../assets/images/plus.svg";

export default {
  data: () => ({
    cards: [
      {
        img: img1,
        title: "Turli o’lchamdagi <br/> samokleykalar",
      },
      {
        img: img2,
        title: "Tekstil mahsulotlari uchun upakovkalar",
      },
      {
        img: img3,
        title: "Qurilish materiallari uchun upakovkalar",
      },
      {
        img: img4,
        title: "Vakuumli upakovkalar",
      },
      {
        img: img5,
        title: "Turli xil oziq ovqat mahsulotlari uchun upakovkalar",
      },
      {
        img: img6,
        title: "Laminatsiya xizmati",
      },
      {
        img: img7,
        title: "Kesib berish xizmati",
      },
      {
        img: img8,
        title: "Glubokiy pechat xizmati",
      },
    ],
    plus: [
      {
        img: img,
        class: "plusone",
      },
      {
        img: img,
        class: "plustwo",
      },
      {
        img: img,
        class: "plusthree",
      },
    ],
  }),
};
</script>
<style lang="scss" scoped>
section.about {
  padding-top: 150px;
  background: #fff;
  padding-bottom: 80px;
}
h1 {
  font-style: normal;
  font-weight: bold;
  font-size: 32px;
  line-height: 37px;
  color: #000000;
  margin-bottom: 94px;
}
img {
  max-width: 100%;
  height: auto;
  margin-bottom: 40px;
}
h3 {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 24px;
  line-height: 130%;
  text-align: center;
}
img.plusone {
  position: absolute;
  left: 0;
  top: 50%;
  z-index: 2;
  transform: translateY(-50%);
}
img.plustwo {
  position: absolute;
  left: 0;
  top: 50%;
  z-index: 2;
  transform: translateY(-50%);
}
img.plusthree {
  position: absolute;
  left: 0;
  top: 50%;
  z-index: 2;
  transform: translateY(-50%);
}
</style>
