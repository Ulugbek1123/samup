<template>
  <v-app>
    <v-app-bar app color="white" height="120px" style="z-index:100;">
      <div
        style="width:100%;"
        class="d-flex justify-center align-center toolbar_nav"
      >
        <v-app-bar-nav-icon
          class="toolbar_icon d-blok_xs"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
        <v-btn
          tag="a"
          class="nav_link sam-link"
          style="font-size:20px"
          v-for="n in buttonLeft"
          :key="n.name"
          :href="n.href"
          depressed
          color="transparent"
        >
          {{ n.name }}
        </v-btn>
        <a href="/">
          <img
            alt="star Logo"
            class="shrink mx-8 logoHeader d-none_Logomd btnSrc"
            style="flex: 0 0 auto; "
            :src="require('./assets/logo yellow 1.png')"
          />
        </a>
        
        <v-btn
          tag="a"
          class="nav_link sam-link"
          :style="`font-size:20px; font-weight:${n.weight};`"
          v-for="n in buttonRight"
          :key="n.name"
          depressed
          color="transparent"
          :href="n.href"
        >
          {{ n.name }}
        </v-btn>
        <v-btn
          :style="`font-size:20px;`"
          tag="a"
          href="tel:+99898 190 60 70"
          depressed
          color="transparent"
          class="d-block_sm d-none_xs"
        >
          +99898 190 60 70
        </v-btn>
        <v-btn
          tag="a"
          href="tel:+99898 190 60 70"
          class="mx-2 d-block_xs phones"
          fab
          dark
          color="warning"
        >
          <v-icon dark>
            mdi-phone
          </v-icon>
        </v-btn>
      </div>
    </v-app-bar>
    <v-main>
      <v-navigation-drawer v-model="drawer" fixed temporary style="top: 120px;">
        <v-list dense>
          <v-list-item tag="a" class="sam-link" :href="item.href" v-for="item in drawers" :key="item.name" link>
            <v-list-item-content>
              <v-list-item-title :src-data="item.href">{{ item.name }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <Header />
      <About />
      <services />
      <Portfolio />
      <Client />
      <Map />
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/header";
import About from "./components/about";
import services from "./components/services";
import Portfolio from "./components/portfolio";
import Client from "./components/Client";
import Map from "./components/Map";
import Footer from "./components/Footer";
import $ from 'jquery'
export default {
  name: "App",

  components: { Header, About, services, Portfolio, Client, Map, Footer },
  mounted () {
    let links = ('.sam-link');
    $(links).on('click', function (e) {
        e.preventDefault();
        let id = $(this).attr('href');
        let target = $(id).offset().top;
        $('html, body').animate({
            scrollTop: target,
        }, 1000);
    });
  },
  data: () => ({
    drawer: false,
    drawers: [
      {
        name: "Biz haqimizda",
        href:'#about',
      },
      {
        name: "Xizmatlarimiz",
        href:'#services',
      },
      {
        name: "Portfolio",
        href:'#portfolio',
      },
      {
        name: "Mijozlarimiz",
        href:'#client',
      },
      {
        name: "Kontaktlarimiz",
        href:'#footer',
      },
    ],
    buttonLeft: [
      {
        name: "Biz haqimizda",
        href:'#about',
      },
      {
        name: "Xizmatlarimiz",
        href:'#services',
      },
      {
        name: "Portfolio",
        href:'#portfolio',
      },
    ],
    buttonRight: [
      {
        name: "Mijozlarimiz",
        href:'#client',
      },
      {
        name: "Kontaktlarimiz",
        href:'#footer',
      },
    ],
  }),
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700;800&display=swap");
.v-navigation-drawer--is-mobile:not(.v-navigation-drawer--close),
.v-navigation-drawer--temporary:not(.v-navigation-drawer--close) {
  box-shadow: none !important;
}
.v-toolbar__content .v-btn.v-btn--icon.v-size--default,
.v-toolbar__extension .v-btn.v-btn--icon.v-size--default {
  width: 85px !important;
  height: 85px !important;
}
.v-btn--icon.v-size--default .v-icon,
.v-btn--fab.v-size--default .v-icon {
  font-size: 80px;
}

.v-btn--fab.v-size--default .v-icon {
  font-size: 24px !important;
}

.d-block_xs {
  display: none;
}
.d-block_sm {
  display: inline-flex;
}
.d-blok_xs{
  display: none;
}
@media (max-width: 1400px) {
  .nav_link {
    font-size: 17px !important;
  }
}
@media (max-width: 1263px) {
  .nav_link {
    display: none;
  }
.d-blok_xs{
  display: block;
}
  .d-block_sm {
    display: block;
  }
  .toolbar_nav.justify-center {
    justify-content: space-between !important;
  }
  .logoHeader {
    margin-right: 0px !important;
    margin-left: 0px !important;
  }
}
@media (max-width: 599px) {
  .d-none_xs {
    display: none;
  }
  .d-block_xs.phones {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .v-toolbar__content .v-btn.v-btn--icon.v-size--default,
  .v-toolbar__extension .v-btn.v-btn--icon.v-size--default {
    width: 45px !important;
    height: 45px !important;
  }
  .v-btn--icon.v-size--default .v-icon,
  .v-btn--fab.v-size--default .v-icon {
    font-size: 40px;
  }
}
</style>
