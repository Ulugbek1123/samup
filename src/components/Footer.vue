<template>
  <footer id="footer">
    <v-container>
      <v-row>
        <v-col class="text-center" cols="12" md="4">
          <div class="logo">
            <img :src="require('../assets/logo black 1.png')" alt="" />
            <div class="icons d-flex justify-space-between align-center">
              <a href="#!">
                <img
                  :src="require('../assets/footerLogo/telegram.svg')"
                  alt=""
                />
              </a>
              <a href="#!">
                <img
                  :src="require('../assets/footerLogo/facebook.svg')"
                  alt=""
                />
              </a>
              <a href="#!">
                <img
                  :src="require('../assets/footerLogo/instagram.svg')"
                  alt=""
                />
              </a>
            </div>
          </div>
        </v-col>
        <v-col
          class="text-center d-flex justify-center flex-column align-center"
          cols="12"
          md="4"
        >
          <h3 class="d-flex justify-center align-center">
            <img
              :src="require('../assets/footerLogo/map.svg')"
              class="mr-2"
              alt=""
            />
            Manzil
          </h3>
          <ul>
            <li>Samarqand shahar</li>
            <li>Samarqand tuman</li>
            <li>Guliston mahallasi</li>
          </ul>
        </v-col>
        <v-col
          class="text-center d-flex justify-center flex-column align-center"
          cols="12"
          md="4"
        >
          <h3 class="d-flex justify-center align-center">
            <img
              :src="require('../assets/footerLogo/phone.svg')"
              class="mr-2"
              alt=""
            />
            Telefonlarimiz
          </h3>
          <ul>
            <li><a href="tel:+99898 190 60 70">+99898 190 60 70</a></li>
            <li><a href="tel:+99899 597 60 70">+99899 597 60 70</a></li>
            <li><a href="tel:+99891 524 60 70">+99891 524 60 70</a></li>
          </ul>
        </v-col>
      </v-row>
    </v-container>
    <div class="footer">
        <v-container>
          <v-row>
            <v-col cols="12" md="6" class="footer_col">
              <p>
                Copyright © 2020 Samarqand Upakovshik. All rights reserved.
              </p>
            </v-col>
            <v-col cols="12" md="6" class="footer_col_2">
              <p>
                Developed by <a href="https://cloud9.uz">Cloud9 ITcompany</a>
              </p>
            </v-col>
          </v-row>
        </v-container>
      </div>
  </footer>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
* {
  list-style: none;
  text-decoration: none;
}
footer {
  background: #f2f2f2;
  padding-top: 20px;
}
.icons {
  width: 34%;
  margin: 30px auto 0px auto;
}
ul > li {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 20px;
  line-height: 27px;
  text-align: center;
  color: #000000;
  a {
    color: #000;
  }
}
ul {
  margin-top: 20px;
}
.footer {
  background: #D6D6D6;
  &_col {
    display: flex;
    justify-content: start;
    align-items: center;
  }
  &_col_2 {
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
}
@media (max-width:959px) {
  .footer {
  background: #D6D6D6;
  &_col {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &_col_2 {
    display: flex;
    justify-content:center;
    align-items: center;
  }
}
}
</style>
