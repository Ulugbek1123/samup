<template>
  <section class="about" id="about">
    <h1 class="text-center">Kompaniyamiz haqida</h1>
    <v-container>
      <v-row>
        <v-col cols="12" md="6" class="d-flex justify-center align-center">
          <img :src="require('../assets/images/about.jpg')" alt="" />
        </v-col>
        <v-col cols="12" md="6" class="d-flex justify-center align-center">
          <v-row>
            <v-col cols="12" sm="7">
              <p>
                Samarqand Upakovshik kompaniyasi - bu biznesingiz yanada
                rivojlanishi va muvaqqiyatga erishishidagi ishonchli hamkor.
                Kompaniyamiz buning uchun eng zamonaviy texnologiyalar va
                tajribali jamoa bilan o’z xizmatlarini taklif qilishdan benihoya
                xursand.
              </p>
            </v-col>
            <v-col cols="12" sm="5">
              <p>
                Sizning mahsulotlaringizga zamonaviy dizayn va qadoqlar
                yaratish, yetkazib berish, bu orqali savdoingizni
                oshirishingizda bor imkoniyatlarini berishga tayyor.
              </p>
            </v-col>
            <v-col cols="12">
              <p>
                Kompaniyamizning asosiy faoliyati turli xil oziq-ovqat va boshqa
                mahsulotlar uchun qadoqlash materialini ishlab chiqarishdan
                iborat. O'zbekiston Respublikasida 3 yildan ortiq vaqtdan buyon
                faoliyat yuritar ekan, kompaniya professionallik, yuqori
                darajada tayyorlanganlik hamda o'zaro manfaatli shartlarda
                sifatli, raqobatbardosh mahsulot ishlab chiqarish orqali
                tanildi.
              </p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
section.about {
  padding-top: 40px;
  background: #f2f2f2;
  padding-bottom: 80px;
}
h1 {
  font-style: normal;
  font-weight: bold;
  font-size: 32px;
  line-height: 37px;
  color: #000000;
  margin-bottom: 40px;
}
img {
  max-width: 100%;
  height: auto;
}
p {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 17px;
  line-height: 150%;
  color: #000000;
  position: relative;
}
p::after {
  position: absolute;
  top: -10px;
  left: 0;
  content: "";
  display: block;
  width: 160px;
  height: 2px;
  background: #feda1b;
}
</style>
