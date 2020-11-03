<template>
  <v-app>
    <v-container
      class="hero"
      fluid
    >
      <v-row>
        <v-app-bar-nav-icon
          class="navicon"
          color="primary"
          background-color="transparent"
          @click.stop="drawer = !drawer"
        />
        <v-navigation-drawer
          v-model="drawer"
          absolute
          temporary
        >
          <v-list
            nav
            dense
          >
            <v-list-item-group>
              <v-list-item v-for="(item, index) in menu" :key="index" :href="item.url">
                <v-list-item-title>{{ item.name }}</v-list-item-title>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-navigation-drawer>
        <v-col
          sm="3"
          md="2"
        >
          <a href="/" class="icon__anchor">
            <h1 class="icon">Pablo</h1>
          </a>
        </v-col>
        <v-col
          class="ml-auto"
          sm="9"
          offset-sm="0"
        >
          <v-tabs
            class="tabs"
            right
            background-color="transparent"
          >
            <v-tabs-slider color="transparent" />
            <v-tab v-for="(item,index) in menu" :key="index" :href="item.url">
              <p class="tabs__item">
                {{ item.name }}
              </p>
            </v-tab>
          </v-tabs>
        </v-col>
      </v-row>
      <v-row>
        <v-col
          sm="10"
          offset-md="6"
          md="9"
        >
          <div>
            <h1 class="hero__title">
              {{ title }}
            </h1>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <nuxt />
    <footer>
      <v-tabs
        fixed-tabs
        background-color="#FBC02D"
        class="footer__tabs"
      >
        <v-tabs-slider color="transparent" />
        <v-tab v-for="(item,index) in menu" :key="index" :href="item.url" class="tabs__item">
          <p class="tabs__item">
            {{ item.name }}
          </p>
        </v-tab>
        <p class="footer__copy mr-4">
          &copy; 2020 pablo
        </p>
      </v-tabs>
      <p class="footer__copy2 mr-4">
        &copy; 2020 pablo
      </p>
    </footer>
  </v-app>
</template>

<script>
const menuitem = [
  {
    name: 'ホーム',
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
    name: 'お問い合わせ',
    url: '/inquiry/',
    icon: 'mdi-heart'
  }
]
export default {
  name: 'Slayout',
  props: {
    // eslint-disable-next-line vue/require-default-prop
    title: String
  },
  data () {
    return {
      menu: menuitem,
      drawer: false
    }
  }
}

</script>
<style scoped>
.icon__anchor {
  text-decoration:none;
}
@media screen and (max-width: 420px){
  .icon__anchor {
    display: none;
  }
}
@media screen and (min-width: 420px){
  .navicon {
    display: none;
  }
}
.icon {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-size: 50px;
  color: #FBC02D;
}
@media screen and (max-width: 420px){
  .icon {
  width: 130px;
  height: 60px;
  margin: 0px 0px 0px 180px;
  }
}
@media screen and (max-width: 420px) {
  .tabs {
    display: none;
  }
}
.tabs__item {
  color: aliceblue;
  font-size: 15px;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-weight: bold;
}
.hero {
  background-image: url('/3888153_s.jpg');
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 50vh;
}
.hero__title {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-size: 7vw;
  color: white;
}
.hero__text {
  color:white;
  font-size: 4vw;
}
@media screen and (max-width: 400px){
  .hero {
  background-image: url('/3888153_s.jpg');
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 50vh;
}
  .hero__title {
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-size: 10vh;
    margin: 50px 5px 0px 0px ;
    height: 25vh;
    color: white;
}
.hero__text {
  color:white;
  font-size: 20px;
  margin: 0px 0px 300px 0px;
}
}
.v-toolbar__title{
  font-size: 60px;
}
@media screen and (max-width: 420px){
  .footer__tabs{
    display: none;
  }
}
.footer__copy{
  margin-top: 20px;
  color: white;
}
.footer__copy2 {
  color: #FBC02D;
}
@media screen and (min-width: 420px){
  .footer__copy2{
    display: none;
  }
}
</style>
