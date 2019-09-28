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
        <div class="introduction">
          <p>平日はエンジニア、週末になると山に登る人</p>
          <p>最高到達地点はキナバル(4095m) 、エンジニアとしても山界に貢献したくて模索中</p>
          <p>将来の目標：ニュージーランドに移住</p>
          <p>好きな山：北岳、間ノ岳を中心に南アルプスによく行きます</p>
          <p>旅先：🇯🇵🇩🇪🇰🇷🇹🇼🇲🇾</p>
        </div>
      </div>
      <div class="sns_link">
        <div class="yamap">
          <a href="https://yamap.com/users/436203" target="_blank">
            <div class="yamap_button">
              <img class="icon_yamap" src="../assets/images/icon_yamap.png" />
            </div>
          </a>
        </div>
        <div class=twitter>
          <a href="https://https://twitter.com/shiki_climber" target="_blank">
            <div class="twitter_button">
              <img class="icon_twitter" src="../assets/images/icon_twitter.png" />
            </div>
          </a>
        </div>
        <!-- TODO: ADD Instagram Icon -->
        <!-- <div class="instagram"></div> -->
      </div>
  </v-layout>
</template>

<script>

export default {
  components: {
  }
}
</script>

<style>
.profile {
  text-align: center;
}

.profile img {
  margin-top: 5%;
  border-radius: 200px;
  width: 200px;
  height: 200px;
}

.introduction {
  text-align: center;
  margin-top: 7%;
}

.sns_link {
  text-align: center;
}

.sns_link img {
  width: 35px;
  border-radius: 35px;
}

.yamap {
  display: inline-block;
}

.twitter {
  display: inline-block;
}
</style>
