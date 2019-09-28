<template>
  <v-container>
  <v-simple-table fixed-header height="600px">
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">山名</th>
          <th class="text-left">画像</th>
          <th class="text-left">登頂日</th>
          <th class="text-left">天気</th>
          <th class="text-left">人数</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="mountain in mountains" :key="mountain.name">
          <td>{{ mountain.name }}</td>
          <td><v-img :src="mountain.image" aspect-ratio="1.7"></v-img></td>
          <td>{{ mountain.date }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
            mountains: [
                { name: "石鎚山", image: require("../assets/images/mountains/ishizuchisan.jpeg"), date: "2013.10.12"},
                { name: "大山", image: require("../assets/images/mountains/daisen.jpeg"), date: "2015.09.20"},
                { name: "立山", image: require("../assets/images/mountains/tateyama.jpeg"), date: "2015.09.24"},
                { name: "祖母山", image: require("../assets/images/mountains/sobosan.jpeg"), date: "2015.10.17"},
                { name: "九重山", image: require("../assets/images/mountains/kuzyusan.jpeg"), date: "2015.10.18"},
                { name: "伊吹山", image: require("../assets/images/mountains/ibukiyama.jpg"), date: "2016.05.02"},
                { name: "塔ノ岳", image: require("../assets/images/mountains/tonodake.jpg"), date: "2016.06.19"},
                { name: "丹沢山", image: require("../assets/images/mountains/tanzawasan.jpg"), date: "2016.06.19"},
                { name: "槍ヶ岳", image: require("../assets/images/mountains/yarigatake.jpeg"), date: "2016.09.30"},
                { name: "那須岳", image: require("../assets/images/mountains/nasudake.jpg"), date: "2016.10.10"},
                { name: "北岳", image: require("../assets/images/mountains/kitadake.jpeg"), date: "2016.10.15"},
                { name: "大岳山", image: require("../assets/images/mountains/otakesan.jpeg"), date: "2017.04.29"},
                { name: "大菩薩嶺", image: require("../assets/images/mountains/daibosaturei.jpeg"), date: "2017.05.05"},
                { name: "乾徳山", image: require("../assets/images/mountains/kentokusan.jpg"), date: "2017.06.17"},
                { name: "三ツ峠山", image: require("../assets/images/mountains/mitsutogeyama.jpg"), date: "2017.07.02"},
                { name: "仙丈ヶ岳", image: require("../assets/images/mountains/senzyogatake.jpg"), date: "2017.07.15"},
                { name: "白山", image: require("../assets/images/mountains/hakusan.jpg"), date: "2017.08.05"},
                { name: "甲斐駒ヶ岳", image: require("../assets/images/mountains/kaikomagatake.jpeg"), date: "2017.08.20"},
                { name: "北岳", image: require("../assets/images/mountains/kitadake2.jpg"), date: "2017.09.09"},
                { name: "間ノ岳", image: require("../assets/images/mountains/ainodake.jpg"), date: "2017.09.10"},
                { name: "筑波山", image: require("../assets/images/mountains/tukubasan.jpeg"), date: "2018.03.25"},
                { name: "武甲山", image: require("../assets/images/mountains/bukosan.jpeg"), date: "2018.04.01"},
                { name: "三頭山", image: require("../assets/images/mountains/mitosan.jpeg"), date: "2018.04.18"},
                { name: "宮之浦岳", image: require("../assets/images/mountains/miyanouradake.jpeg"), date: "2018.04.29"},
                { name: "塔ノ岳", image: require("../assets/images/mountains/tonodake2.jpg"), date: "2018.05.12"},
                { name: "男体山", image: require("../assets/images/mountains/nantaisan.jpg"), date: "2018.05.26"},
                { name: "谷川岳", image: require("../assets/images/mountains/tanigawadake.jpg"), date: "2018.06.02"},
                { name: "硫黄岳", image: require("../assets/images/mountains/iodake.jpeg"), date: "2018.06.30"},
                { name: "横岳", image: require("../assets/images/mountains/yokodake.jpeg"), date: "2018.07.01"},
                { name: "赤岳", image: require("../assets/images/mountains/akadake.jpeg"), date: "2018.07.01"},
                { name: "幕山", image: require("../assets/images/mountains/makuyama.jpg"), date: "2019.02.23"},
                { name: "塔ノ岳", image: require("../assets/images/mountains/tonodake3.jpg"), date: "2019.03.02"},
                { name: "竜ヶ岳", image: require("../assets/images/mountains/ryugadake.jpg"), date: "2019.03.09"},
                { name: "キナバル山", image: require("../assets/images/mountains/kinabaru.jpg"), date: "2019.04.28"},
                { name: "金峰山", image: require("../assets/images/mountains/kinpusan.jpg"), date: "2019.06.01"},
                { name: "瑞牆山", image: require("../assets/images/mountains/mizugakiyama.jpg"), date: "2019.06.02"},
                { name: "北岳", image: require("../assets/images/mountains/kitadake3.jpg"), date: "2019.07.26"},
                { name: "石鎚山", image: require("../assets/images/mountains/ishizuchisan2.jpg"), date: "2019.08.11"},
                { name: "薬師岳", image: require("../assets/images/mountains/yakushidake.jpg"), date: "2019.08.17"},
                { name: "観音岳", image: require("../assets/images/mountains/kannondake.jpg"), date: "2019.08.17"},
                { name: "地蔵岳", image: require("../assets/images/mountains/zizodake.jpg"), date: "2019.08.18"},
                { name: "白馬岳", image: require("../assets/images/mountains/shiroumadake.jpg"), date: "2019.08.24"},
                { name: "小蓮華山", image: require("../assets/images/mountains/korengesan.jpg"), date: "2019.08.25"},
                { name: "乗鞍岳", image: require("../assets/images/mountains/norikuradake.jpg"), date: "2019.08.25"},
                { name: "燕岳", image: require("../assets/images/mountains/tsubakurodake.jpg"), date: "2019.09.14"},
                { name: "大天井岳", image: require("../assets/images/mountains/otenshodake.jpg"), date: "2019.09.15"},
                { name: "常念岳", image: require("../assets/images/mountains/zyonendake.jpg"), date: "2019.09.16"},
                { name: "蝶ヶ岳", image: require("../assets/images/mountains/cyogadake.jpg"), date: "2019.09.16"},
                { name: "焼岳", image: require("../assets/images/mountains/yakedake.jpg"), date: "2019.09.25"},
            ]

      }
    }
  }
</script>

<style>
</style>