<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
      class="hidden-md-and-up"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar fixed app flat color="grey lighten-5">
      <div class="side-bar-icon">
        <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer" />
      </div>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="(item, i) in items" :key="i" :to="item.to" text append>
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-content>
      <transition name="fade">
        <div class="content">
          <nuxt />
        </div>
      </transition>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  components: {
  },
  data() {
    return {
      clipped: false,
      drawer: false,
      items: [
        { title: 'Top', to: '/' },
        { title: 'Mountains', to: '/mountains' },
        { title: 'Profile', to: '/profile' },
        { title: 'Blogs', to: '/blogs' },
      ],
      title: "Shiki WeekendClimber"
    }
  }
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}

.v-toolbar {
  margin-top: 70px !important;
}

.content {
  margin-top: 55px;
}

.v-btn {
  /* text-decoration : underline !important; */
}
.v-btn:before {
  opacity: 0 !important;
}
/* 
.side-bar-icon {
  padding-top: 30px;
} */
</style>