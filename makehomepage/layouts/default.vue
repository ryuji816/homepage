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
          <h1 class="hero__title">
            Pablo
          </h1>
          <p class="hero__text">
            神戸大学プログラミングサークル
          </p>
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
        <v-tab v-for="(item,index) in menu" :key="index" :href="item.url" class="tabs__item__footer">
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
  name: 'TopLayout',
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
@media screen and (max-width: 400px){
  .icon__anchor {
    display: none;
  }
}
.icon {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-size: 50px;
  color: #FBC02D;
}
@media screen and (max-width: 400px){
  .icon {
  width: 130px;
  height: 60px;
  margin: 0px 0px 0px 180px;
  }
}
@media screen and (min-width: 400px){
  .navicon {
    display: none;
  }
}
@media screen and (max-width: 400px) {
  .tabs {
    display: none;
  }
}
.tabs__item__footer {
  color: brown;
  font-size: 15px;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-weight: bold;
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
  height: 100vh;
}
.hero__title {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-size: 20vw;
  color: #FBC02D;
}
.hero__text {
  color:white;
  font-size: 4vw;
}
@media screen and (max-width: 400px){
  .hero__title {
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-size: 15vh;
    margin: 200px 5px 0px 0px ;
    height: 25vh;
    color: #FBC02D;
}
.hero__text {
  color:white;
  font-size: 20px;
  margin: 0px 0px 300px 0px;
}
}
@media screen and (max-width: 400px){
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
@media screen and (min-width: 400px){
  .footer__copy2{
    display: none;
  }
}
</style>
