<template>
  <v-app>
    <v-app-bar dense>
      <v-app-bar-nav-icon @click="drawer=true" />
      <v-toolbar-title @click="back_home">
        プログラミングサークルPablo
      </v-toolbar-title>
      <v-tabs icons-and-text>
        <v-tabs-slider />
        <v-tab v-for="(item,index) in menu" :key="index" :href="item.url">
          {{ item.name }}
        </v-tab>
      </v-tabs>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" fixed temporary>
      <v-list rounded>
        <v-list-group>
          <v-list-item v-for="(item, index) in menu" :key="index" :href="item.url">
            <v-list-title v-text="item.name" />
          </v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
    <v-container fluid>
      <nuxt />
    </v-container>
    <footer>
      <v-tabs
        fixed-tabs
        background-color="indigo"
        dark
      >
        <v-tabs-slider />
        <v-tab v-for="(item,index) in menu" :key="index" :href="item.url">
          {{ item.name }}
        </v-tab>
      </v-tabs>
      &copy; 2020 pablo
    </footer>
  </v-app>
</template>

<script>
const menuitem = [
  {
    name: 'HOME',
    url: '/',
    icon: 'mdi-heart'
  },
  {
    name: '活動内容',
    url: '/activity/',
    icon: 'mdi-heart'
  },
  {
    name: '成果物',
    url: '/results/',
    icon: 'mdi-heart'
  },
  {
    name: '年間予定',
    url: '/schedule/',
    icon: 'mdi-heart'
  },
  {
    name: 'サークル概要',
    url: '/detail/',
    icon: 'mdi-heart'
  },
  {
    name: 'お問い合わせ',
    url: '/inquiry/',
    icon: 'mdi-heart'
  }
]
export default {
  data () {
    return {
      menu: menuitem,
      drawer: false
    }
  },
  methods: {
    back_home () {
      this.$router.push('/')
    }
  }
}

</script>
<style scoped>
.v-toolbar__title{
  overflow: visible;
  margin: 20px;

}
</style>
