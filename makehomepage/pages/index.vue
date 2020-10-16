<template>
  <v-app>
    <v-container
      class="hero pa-10"
      fill-height
      fluid
    >
      <v-row>
        <v-col
          align-self="center"
        >
          <h1 class="hero_title">
            Pablo
          </h1>
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row>
        <v-col
          md="7"
        >
          <h1>News</h1>
          <v-carousel
            cycle
            hide-delimiters
          >
            <v-carousel-item
              v-for="(slide, index) in slides"
              :key="index"
              :src="slide.url"
            >
              <h1>{{ slide.name }}</h1>
            </v-carousel-item>
          </v-carousel>
        </v-col>
        <v-col
          align-self="end"
          justify="end"
        >
          <v-sheet
            color="red lighten-1"
            elevation="10"
            height="70"
            width="400"
          >
            <div class="text-center text-h4 ">
              <span class="black--text">受託開発受け付けます</span>
              <v-btn
                class="mx-2"
                fab
                large
                color="yellow lighten-1"
                href="/inquiry/"
              >
                <v-icon dark>
                  mdi-arrow-right
                </v-icon>
              </v-btn>
            </div>
          </v-sheet>
        </v-col>
      </v-row>
    </v-container>
    <v-container
      class="overview"
      fill-height
      fluid
    >
      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <v-card>
            <v-img src="/pablo.png" height="400" />
          </v-card>
        </v-col>
        <v-col
          offset="1"
          md="5"
        >
          <v-sheet
            color="orange lighten-1"
            elevation="10"
            height="70"
            width="500"
          >
            <div class="text-h2 text-center">
              <span class="black--text">サークル概要</span>
            </div>
          </v-sheet>
          <hr>
          <p
            class="text-justify text--secondary overview_text"
          >
            「情報技術の発達の激しい社会の中で、適切な技術を提供できる人材を育成したい」プログラミングサークルPabloはこのような理念の
            もと、日々活動しています。サークルとしてメンバー同士で協力しあうことで、また大学生ならではの発想でメンバーにとっても社会にとっても
            様々な価値を提供していきたいと考えています。
          </p>
          <v-btn
            class="mx-2"
            fab
            large
            color="yellow lighten-1"
            href="/detail/"
          >
            <v-icon dark>
              mdi-arrow-right
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
    <v-container
      class="activitie"
      fill-height
      fluid
    >
      <v-row>
        <v-col
          md="5"
        >
          <v-sheet
            color="blue lighten-1"
            elevation="10"
            height="70"
            width="500"
          >
            <div class="text-h2 text-center">
              <span class="black--text">活動内容</span>
            </div>
          </v-sheet>
          <hr>
          <p class="text--secondary">
            サークルでは以下の活動を行っています。
          </p>
          <ul class="activities text--secondary">
            <li>もくもく会</li>
            <li>競技プログラミング振り返り会</li>
            <li>自主ゼミ</li>
            <li>自社開発</li>
            <li>受託開発</li>
          </ul>
          <v-btn
            class="mx-2"
            fab
            large
            color="yellow lighten-1"
            href="/activity/"
          >
            <v-icon dark>
              mdi-arrow-right
            </v-icon>
          </v-btn>
        </v-col>
        <v-spacer />
        <v-col
          cols="12"
          md="6"
        >
          <v-card>
            <v-img src="/pablo.png" />
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <v-container
      class="result"
      fill-height
      fluid
    >
      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <v-card>
            <v-img src="/pablo.png" height="400" />
          </v-card>
        </v-col>
        <v-col
          md="5"
          offset="1"
        >
          <v-sheet
            color="green lighten-1"
            elevation="10"
            height="70"
            width="500"
          >
            <div class="text-h2 text-center">
              <span class="black--text">成果物・実績</span>
            </div>
          </v-sheet>
          <hr>
          <p class="results text--secondary">
            サークルには、様々な背景を持ったメンバーが所属しています。そのメンバーが各々の興味のある分野について学習した記録を共有するために
            まとめています。
          </p>
          <p class="results text--secondary">
            また、サークルとして、共同で開発した成果物についても紹介します。
          </p>
          <p />
          <v-btn
            class="mx-2"
            fab
            large
            color="yellow lighten-1"
            href="/results/"
          >
            <v-icon dark>
              mdi-arrow-right
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
const cyima = [
  {
    name: 'News1',
    url: '/1.png'
  },
  {
    name: 'News2',
    url: '/2.png'
  },
  {
    name: 'News3',
    url: '/3.png'
  }
]

export default {
  data () {
    return {
      slides: cyima
    }
  }
}
</script>

<style scoped>
.hero {
  background-image: url('/3888153_s.jpg');
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 100vh;
}
.hero_title {
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-size: 20vh;
    color: yellow;
}
.overview {
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 90vh;
}
.overview_title {
  font-family: 'Courier New', Courier, monospace;
  font-size: 50px;
  color: crimson;
}
.overview_text {
  font-size: 16px;
  line-height: 30px;
}
.activitie {
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 90vh;
}
.activities {
  line-height: 30px;
}
.result {
    background-color:whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 90vh;
}
.results {
  line-height: 30px;
}
</style>
