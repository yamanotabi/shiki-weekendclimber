<template>
  <v-container>
    <div class="page-title">
      <h4>山行履歴</h4>
    </div>
    <!-- <div class=weather-data> -->
      <!-- <h3>天気情報</h3> -->
      <!-- <div class=sunny>晴れ: 77.55%</div>
      <div class=cloudy>曇り: 18.37%</div>
      <div class=rain>雨: 4.08%</div> -->
    <!-- </div> -->
    <v-simple-table fixed-header height="600px">
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Name</th>
            <th class="text-left">Height(m)</th>
            <th class="text-left">Photo</th>
            <th class="text-left">Date</th>
            <th class="text-left">Weather</th>
            <th class="text-left">Party</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="mountain in mountains" :key="mountain.id">
            <td>{{ mountain.name }}</td>
            <td>{{ mountain.height }}</td>
            <td><v-img :src="mountain.image" aspect-ratio="1.5"></v-img></td>
            <td style="white-space:pre-wrap; word-wrap:break-word;">{{ mountain.date }}</td>
            <td style="white-space:pre-wrap; word-wrap:break-word;">{{ mountain.weather }}</td>
            <td style="white-space:pre-wrap; word-wrap:break-word;">{{ mountain.number }}</td>
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
            { id: 0, name: "石鎚山", height: "1,982", image: require("../assets/images/mountains/ishizuchisan2.jpg"), date: "2013.10.12\n2019.08.11", weather: "晴れ\n晴れ", number: "6人\n2人"},
            { id: 1, name: "大山", height: "1,729", image: require("../assets/images/mountains/daisen.jpeg"), date: "2015.09.20\n2019.10.27", weather: "晴れ\n曇り", number: "2人\nソロ"},
            { id: 2, name: "立山", height: "3,015", image: require("../assets/images/mountains/tateyama.jpeg"), date: "2015.09.24", weather: "曇り", number: "ソロ"},
            { id: 3, name: "祖母山", height: "1,756", image: require("../assets/images/mountains/sobosan.jpeg"), date: "2015.10.17", weather: "晴れ", number: "ソロ"},
            { id: 4, name: "九重山", height: "1,791", image: require("../assets/images/mountains/kuzyusan.jpeg"), date: "2015.10.18", weather: "晴れ", number: "ソロ"},
            { id: 5, name: "伊吹山", height: "1,377", image: require("../assets/images/mountains/ibukiyama.jpg"), date: "2016.05.02", weather: "晴れ", number: "ソロ"},
            { id: 6, name: "丹沢山", height: "1,673", image: require("../assets/images/mountains/tanzawasan.jpg"), date: "2016.06.19\n2018.05.12\n2019.03.02", weather: "晴れ\n晴れ\n晴れ", number: "ソロ\n6人\nソロ"},
            { id: 7, name: "槍ヶ岳", height: "3,180", image: require("../assets/images/mountains/yarigatake.jpeg"), date: "2016.09.30", weather: "晴れ", number: "ソロ"},
            { id: 8, name: "那須岳", height: "1,917", image: require("../assets/images/mountains/nasudake.jpg"), date: "2016.10.10", weather: "雨", number: "ソロ"},
            { id: 9, name: "北岳", height: "3,193", image: require("../assets/images/mountains/kitadake.jpg"), date: "2016.10.15\n2017.09.09\n2019.07.26", weather: "晴れ\n曇り\n曇り", number: "ソロ\nソロ\nソロ"},
            { id: 10, name: "大岳山", height: "1,267", image: require("../assets/images/mountains/otakesan.jpeg"), date: "2017.04.29", weather: "晴れ", number: "ソロ"},
            { id: 11, name: "大菩薩嶺", height: "2,057", image: require("../assets/images/mountains/daibosaturei.jpeg"), date: "2017.05.05", weather: "晴れ", number: "ソロ"},
            { id: 12, name: "乾徳山", height: "2,031", image: require("../assets/images/mountains/kentokusan.jpg"), date: "2017.06.17", weather: "曇り", number: "ソロ"},
            { id: 13, name: "三ツ峠山", height: "1,785", image: require("../assets/images/mountains/mitsutogeyama.jpg"), date: "2017.07.02", weather: "曇り", number: "ソロ"},
            { id: 14, name: "仙丈ヶ岳", height: "3,033", image: require("../assets/images/mountains/senzyogatake.jpg"), date: "2017.07.15", weather: "晴れ", number: "3人"},
            { id: 15, name: "白山", height: "2,702", image: require("../assets/images/mountains/hakusan.jpg"), date: "2017.08.05", weather: "雨", number: "ソロ"},
            { id: 16, name: "甲斐駒ヶ岳", height: "2,967", image: require("../assets/images/mountains/kaikomagatake.jpeg"), date: "2017.08.20", weather: "曇り", number: "ソロ"},
            { id: 17, name: "間ノ岳", height: "3,190", image: require("../assets/images/mountains/ainodake.jpg"), date: "2017.09.10", weather: "晴れ", number: "ソロ"},
            { id: 18, name: "筑波山", height: "877", image: require("../assets/images/mountains/tukubasan.jpeg"), date: "2018.03.25", weather: "晴れ", number: "ソロ"},
            { id: 19, name: "武甲山", height: "1,304", image: require("../assets/images/mountains/bukosan.jpeg"), date: "2018.04.01", weather: "晴れ", number: "ソロ"},
            { id: 20, name: "三頭山", height: "1,531", image: require("../assets/images/mountains/mitosan.jpeg"), date: "2018.04.18", weather: "晴れ", number: "ソロ"},
            { id: 21, name: "宮之浦岳", height: "1,936", image: require("../assets/images/mountains/miyanouradake.jpeg"), date: "2018.04.29", weather: "晴れ", number: "ソロ"},
            { id: 22, name: "男体山", height: "2,486", image: require("../assets/images/mountains/nantaisan.jpg"), date: "2018.05.26", weather: "晴れ", number: "4人"},
            { id: 23, name: "谷川岳", height: "1,977", image: require("../assets/images/mountains/tanigawadake.jpg"), date: "2018.06.02", weather: "晴れ", number: "2人"},
            { id: 24, name: "八ヶ岳", height: "2,899", image: require("../assets/images/mountains/akadake.jpeg"), date: "2018.07.01", weather: "晴れ", number: "ソロ"},
            { id: 25, name: "幕山", height: "625", image: require("../assets/images/mountains/makuyama.jpg"), date: "2019.02.23", weather: "晴れ", number: "ソロ"},
            { id: 26, name: "竜ヶ岳", height: "1,485", image: require("../assets/images/mountains/ryugadake.jpg"), date: "2019.03.09", weather: "晴れ", number: "ソロ"},
            { id: 27, name: "キナバル山", height: "4,095", image: require("../assets/images/mountains/kinabaru.jpg"), date: "2019.04.28", weather: "晴れ", number: "ソロ"},
            { id: 28, name: "金峰山", height: "2,599", image: require("../assets/images/mountains/kinpusan.jpg"), date: "2019.06.01", weather: "晴れ", number: "ソロ"},
            { id: 29, name: "瑞牆山", height: "2,230", image: require("../assets/images/mountains/mizugakiyama.jpg"), date: "2019.06.02", weather: "晴れ", number: "ソロ"},
            { id: 30, name: "鳳凰三山", height: "2,840", image: require("../assets/images/mountains/zizodake.jpg"), date: "2019.08.18", weather: "晴れ", number: "ソロ"},
            { id: 31, name: "白馬岳", height: "2,932", image: require("../assets/images/mountains/shiroumadake.jpg"), date: "2019.08.24", weather: "曇り", number: "ソロ"},
            { id: 32, name: "小蓮華山", height: "2,766", image: require("../assets/images/mountains/korengesan.jpg"), date: "2019.08.25", weather: "晴れ", number: "ソロ"},
            { id: 33, name: "乗鞍岳", height: "2,469", image: require("../assets/images/mountains/norikuradake.jpg"), date: "2019.08.25", weather: "晴れ", number: "ソロ"},
            { id: 34, name: "燕岳", height: "2,763", image: require("../assets/images/mountains/tsubakurodake.jpg"), date: "2019.09.14", weather: "晴れ", number: "ソロ"},
            { id: 35, name: "大天井岳", height: "2,922", image: require("../assets/images/mountains/otenshodake.jpg"), date: "2019.09.15", weather: "晴れ", number: "ソロ"},
            { id: 36, name: "常念岳", height: "2,857", image: require("../assets/images/mountains/zyonendake.jpg"), date: "2019.09.16", weather: "晴れ", number: "ソロ"},
            { id: 37, name: "蝶ヶ岳", height: "2,677", image: require("../assets/images/mountains/cyogadake.jpg"), date: "2019.09.16", weather: "晴れ", number: "ソロ"},
            { id: 38, name: "焼岳", height: "2,455", image: require("../assets/images/mountains/yakedake.jpg"), date: "2019.09.25", weather: "晴れ", number: "ソロ"},
            { id: 39, name: "木曽駒ヶ岳", height: "2,956", image: require("../assets/images/mountains/kisokomagatake.jpg"), date: "2019.10.05", weather: "晴れ", number: "ソロ"},
            { id: 40, name: "日光白根山", height: "2,578", image: require("../assets/images/mountains/nikkousiranesan.jpg"), date: "2019.10.20", weather: "晴れ", number: "ソロ"},
            { id: 41, name: "武尊山", height: "2,158", image: require("../assets/images/mountains/hotakayama.jpg"), date: "2019.11.02", weather: "晴れ", number: "ソロ"},
            { id: 42, name: "妙義山", height: "1,103", image: require("../assets/images/mountains/myogisan.jpg"), date: "2019.11.17", weather: "晴れ", number: "ソロ"},
            { id: 43, name: "愛鷹山", height: "1,504", image: require("../assets/images/mountains/ashitakayama.jpg"), date: "2019.12.08", weather: "晴れ", number: "ソロ"},
            { id: 44, name: "蓼科山", height: "2,531", image: require("../assets/images/mountains/tateshinayama.jpg"), date: "2019.12.15", weather: "晴れ", number: "4人"},
        ]
      }
    }
  }
</script>

<style>
/* .weather-data {
  margin-top: 10px;
  margin-bottom: 10px;
  text-align: center;
}
.sunny {
  display: inline-block;
}

.cloudy {
  display: inline-block;
}

.rain {
  display: inline-block;
} */

.page-title {
  margin-bottom: 2%;
}
</style>