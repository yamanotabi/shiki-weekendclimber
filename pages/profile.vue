<template>
  <v-layout
    column
    justify-center
  >
    <v-flex
      xs12
    >
    </v-flex>
      <div class="profile">
        <img class="button_img" src="../assets/images/intro_image.jpg" />
        <p class="name">シキ@週末クライマー</p>
        <div class="introduction">
          <p>平日はエンジニア、週末になると山に登る人</p>
          <p>最高到達地点はキナバル(4095m) 、エンジニアとしても山界に貢献したくて模索中</p>
        </div>
      </div>
      <div class="sns_link">
        <div class="sns">
          <p>SNS: </p>
        </div>
        <div class="yamap">
          <a href="https://yamap.com/users/436203" target="_blank" style="color:black;">
            <p>YAMAP</p>
            <!-- <div class="yamap_button">
              <img class="icon_yamap" src="../assets/images/icon_yamap.png" />
            </div> -->
          </a>
        </div>
        <div class=twitter>
          <a href="https://https://twitter.com/shiki_climber" target="_blank" style="color:black;">
            <p>Twitter</p>
            <!-- <div class="twitter_button">
              <img class="icon_twitter" src="../assets/images/icon_twitter.png" />
            </div> -->
          </a>
        </div>
        <!-- TODO: ADD Instagram Icon -->
        <!-- <div class="instagram"></div> -->
      </div>
        <div class="detail">
          <p><b>- プロフィール -</b></p>
          <ul v-for="content in contents" :key="content.id">
            <li><p class="content-question"><b>{{ content.question }}</b></p></li>
            <li><p class="content-answer">{{ content.answer }}</p></li>
          </ul>
        </div>
  </v-layout>
</template>

<script>

export default {
  components: {
  },
  data() {
    return {
      contents: [
        { id: 0, question: "性別", answer: "男" },
        { id: 1, question: "誕生日", answer: "7月30日" },
        { id: 2, question: "星座", answer: "獅子座" },
        { id: 3, question: "血液型", answer: "B型" },
        { id: 4, question: "居住地", answer: "島根県 -> 愛媛県 -> 神奈川県 -> 東京都" },
        { id: 5, question: "職業", answer: "エンジニア" },
        { id: 6, question: "身長", answer: "168cm" },
        { id: 7, question: "体重", answer: "67kg" },
        { id: 8, question: "好きな山", answer: "北岳、間ノ岳を中心に南アルプスによく行きます" },
        { id: 9, question: "旅先", answer: "🇯🇵🇩🇪🇰🇷🇹🇼🇲🇾" },
        { id: 10, question: "座右の銘", answer: "Experience is expensive." },
        { id: 11, question: "好きなことば", answer: "縦走, 稜線, 登頂" },
        { id: 12, question: "好きな映画", answer: "LIFE!" },
        { id: 13, question: "好きな番組", answer: "クレイジージャーニー" },
        { id: 14, question: "好きなブランド", answer: "モンベル, ブラックダイヤモンド, THE NORTH FACE" },
        { id: 15, question: "尊敬する登山家", answer: "竹内洋岳, 中島ケンロウ, 田部井淳子" },
        { id: 16, question: "山アプリ", answer: "YAMAP" },
        { id: 17, question: "好きな異性のしぐさ", answer: "60Lくらいのザックを背負って軽々と山を登っている姿" },
        { id: 18, question: "将来の夢", answer: "山の上で生活する" },
        { id: 19, question: "好きな山域", answer: "南アルプス, 丹沢" },
      ]
    }
  }
}
</script>

<style>
.profile {
  text-align: center;
}

.profile img {
  margin-top: 2%;
  border-radius: 200px;
  width: 200px;
  height: 200px;
}

.introduction {
  text-align: center;
  margin-top: 3%;
  margin-left: 3%;
  margin-right: 3%;
}

.sns_link {
  text-align: center;
}

.sns {
  display: inline-block;
}

.yamap {
  display: inline-block;
}

.twitter {
  display: inline-block;
}

.name {
  margin-top: 1%;
}

a {
  text-decoration: none;
}

.detail {
  margin-left: 5%;
}

ul {
  list-style: none;
}
</style>
