<template>
  <v-container>
    <div class="page-title">
      <p>これまでに制作した山・登山に関するサイト、サービス</p>
    </div>
    <v-layout row wrap>
      <v-flex v-for="(product, i) in products" :key="i" md4 sm4 sx12>
        <v-card>
          <v-img :src="product.image" aspect-ratio="2.75" v-if="product.image != null"></v-img>
          <v-img :src="require('@/assets/images/works/comingsooon.png')" aspect-ratio="1.5" v-else></v-img>
          <v-card-title class="headline">
            {{ product.name }}
          </v-card-title>
          <v-card-text>
            {{ product.description }}
          </v-card-text>
          <v-card-actions>
            <v-btn text :href="product.url" target="_blank" v-if="product.open">
              More
            </v-btn>
            <v-btn text disabled :href="product.url" target="_blank" v-else>
              More
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          name: 'ヤマノコトバ',
          image:
            require("../assets/images/works/yamanokotoba_top.png"),
          description: '山に関するつぶやき、名言を写真と一緒につぶやくことができるサイト',
          url: 'https://yamanokotoba.com/',
          open: true,
        },
        {
          name: "Shiki-WeekendClimber's Page",
          image:
            require("../assets/images/works/shiki-weekendclimber_top.png"),
            description: "自分の登山に関する情報をまとめたポートフォリオサイト",
            url: 'https://shiki-weekendclimber.appspot.com/',
            open: true,
        },
        {
          name: "(仮)Mountains Database",
          image:
            require("../assets/images/works/comingsooon.png"),
            description: "日本の山に関する情報をまとめたデータベース",
            url: '',
            open: true,
        }
      ]
    }
  }
}
</script>

<style>
.v-card {
  margin-right: 2%;
  margin-left: 2%;
  margin-top: 2%;
  margin-bottom: 2%;
}
</style>
