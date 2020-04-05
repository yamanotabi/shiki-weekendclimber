<template>
  <v-layout
    column
    justify-center
  >
    <v-flex
      xs12
    >
    </v-flex>
    <div class="title">
      <h2>Shiki-WeekendClimber's Page</h2>
    </div>
  </v-layout>
</template>

<script>

export default {
  components: {
  },
  head() {
    return {
      title: "Shiki-WeekendClimber's Site",
      meta: [
        { name: 'twitter:card', content: "summary_large_image" },
        { name: 'twitter:site', content: "@shiki_developer" },
        { name: 'twitter:title', content: "Shiki-WeekendClimber's Site"},
        { name: 'twitter:description', content: "shikiの山ポートフォリオサイト" },
        { name: 'twitter:image', content: require('~/assets/images/portfolio_top.png') }
      ]
    }
  },
}
</script>

<style>
.title {
    display: flex;
    justify-content: center;
    margin-top: 20%;
    margin-left: 3%;
    margin-right: 3%;
}

</style>
