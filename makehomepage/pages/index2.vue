<template>
<main>
  <header>
      <v-app-bar>
        <v-app-bar-nav-icon @click="drawer=true"></v-app-bar-nav-icon>
        <v-toolbar-title>プログラミングサークルPablo
        </v-toolbar-title>
        <v-tabs>
          <v-tab v-for="(item,index) in menu" :key="index">
            <nuxt-link :to="item.url">{{ item.name }}</nuxt-link>
          </v-tab>
        </v-tabs>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" fixed temporary>
        <v-list nav dense>
        <v-list-group>
          <v-list-item v-for="(item, index) in menu" :key="index">
            <v-list-title>{{ item.name }}</v-list-title>
          </v-list-item>
        </v-list-group>
        </v-list>
      </v-navigation-drawer>
    </header>
    <body>
      <v-carousel
    cycle
  >
    <v-carousel-item
      v-for="(slide, index) in slides"
      :key="index"
      :src="slide.url"
    >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
        </v-row>
    </v-carousel-item>
  </v-carousel>
  <p></p>
  <v-parallax
    src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg">
    <v-row
      align="start"
      justify="center">
      <v-col
        cols="12">
        <h1>Hello World!!</h1>
        <h2>Let's programing</h2>
        <p>プログラミングサークルPabloは神戸を拠点に活動しています。</p>
        </v-col></v-row>

  </v-parallax>
  <p></p>
  <v-parallax
    src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg">
    <v-row
      align="start"
      justify="center">
      <v-col
        cols="12">
        <h1>Hello World!!</h1>
        <h2>Let's programing</h2>
        <p>プログラミングサークルPabloは神戸を拠点に活動しています。</p>
        </v-col></v-row>

  </v-parallax>
  <p></p>
  <v-parallax
    src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg">
    <v-row
      align="start"
      justify="center">
      <v-col
        cols="12">
        <h1>プログラミングサークルPablo</h1>
        <h4>活動しています</h4>
        </v-col></v-row>

  </v-parallax>
    </body>
    <footer>
        &copy; 2020 pablo
    </footer>

</main>
</template>

<script>
const cyima = [
  {
    name: '活動内容1',
    url: require('@/static/1.png')
  },
  {
    name: '活動内容2',
    url: require('@/static/2.png')
  },
  {
    name: '活動内容3',
    url: require('@/static/3.png')
  }
]
const menuitem = [
  {
    name: 'HOME',
    url: require('@/pages/')
  },
  {
    name: '活動内容',
    url: '/activity/'
  },
  {
    name: '年間予定',
    url: '/schedule/'
  },
  {
    name: '会社概要',
    url: '/detail/'
  },
  {
    name: 'その他',
    url: '/other/'
  }
]
export default {
  data () {
    return {
      slides: cyima,
      menu: menuitem,
      drawer: false
    }
  }
}
</script>

<style scoped>
.v-toolbar__title{
  overflow: visible;
  margin: 50px;

}
</style>
