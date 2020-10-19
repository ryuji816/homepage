<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="6"
          xs="12"
        >
          <v-carousel
            cycle
            hide-delimiters
          >
            <v-carousel-item
              v-for="(slide, index) in slides"
              :key="index"
              :src="slide.url"
              class="carousel"
            />
          </v-carousel>
        </v-col>
        <v-col
          align-self="center"
          justify="end"
        >
          <h1 class="news__title">
            News
          </h1>
          <v-virtual-scroll
            :items="items"
            height="350"
            item-height="70"
          >
            <template v-slot="{ item }">
              <v-list-item>
                <p class="news__date">
                  {{ item.date }}
                </p>
                <v-list-item-action>
                  <div class="news__sort">
                    <p class="news__sort__content">
                      {{ item.genre }}
                    </p>
                  </div>
                </v-list-item-action>

                <v-list-item-content>
                  <v-list-item-title>
                    <strong>{{ item.title }}</strong>
                  </v-list-item-title>
                  <span class="text--secondary">{{ item.content }}</span>
                </v-list-item-content>
              </v-list-item>
            </template>
          </v-virtual-scroll>
          <div class="text-h4 text-center recipient">
            <span class="black--text">開発の相談を受け付けています</span>
            <hr color="#FBC02D">
            <v-btn
              color="purple darken-2"
              href="/inquiry/"
              class="ma-2"
              outlined
            >
              お問い合わせへ
              <v-icon>mdi-arrow-right</v-icon>
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <section class="overview">
      <v-container
        fill-height
      >
        <v-row>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card>
              <v-img src="/IMG_20201017_190326.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h3 text-center">
              <span class="overview__title">サークル理念</span>
            </div>
            <hr color="#FBC02D">
            <p
              class="text-justify content overview_text"
            >
              「情報技術の発達の激しい社会の中で、適切な技術を提供できる人材を育成したい」プログラミングサークルPabloはこのような理念の
              もと、日々活動しています。サークルとしてメンバー同士で協力しあうことで、また大学生ならではの発想でメンバーにとっても社会にとっても
              様々な価値を提供していきたいと考えています。
            </p>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section
      class="activitie"
    >
      <v-container
        class="activitie"
        fill-height
      >
        <v-row>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="activity__title">活動内容</span>
            </div>
            <hr color="#FBC02D">
            <p class="activity__text">
              サークルでは以下の活動を行っています。
            </p>
            <ul class="activity__text">
              <li>もくもく会</li>
              <li>競技プログラミング振り返り会</li>
              <li>自主ゼミ</li>
              <li>自社開発</li>
              <li>受託開発</li>
            </ul>
            <v-btn
              color="purple darken-2"
              href="/activity/"
              class="ma-2"
              outlined
            >
              活動内容へ
              <v-icon>mdi-arrow-right</v-icon>
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card>
              <v-img src="/IMG_20201017_192643.jpg" />
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="result">
      <v-container
        fill-height
      >
        <v-row>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card>
              <v-img src="/image (1).png" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="result__title">成果物・実績</span>
            </div>
            <hr color="#FBC02D">
            <p class="result__text">
              サークルには、様々な背景を持ったメンバーが所属しています。そのメンバーが各々の興味のある分野について学習した記録を共有するために
              まとめています。
            </p>
            <p class="result__text">
              また、サークルとして、共同で開発した成果物についても紹介します。
            </p>
            <p />
            <v-btn
              color="purple darken-2"
              href="/results/"
              class="ma-2"
              outlined
            >
              成果物・実績へ
              <v-icon>mdi-arrow-right</v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </v-app>
</template>

<script>
const news = [
  {
    title: 'ホームページ公開！！',
    content: 'ホームページを作成しました',
    date: '2020/10/19',
    genre: '新着状況'
  },
  {
    title: '競技プログラミング参戦!!',
    content: 'code forceに参加しました',
    date: '2020/10/20',
    genre: '新着状況'
  },
  {
    title: '新しい本の購入!!',
    content: '新しく５冊の本を購入しました',
    date: '2020/10/21',
    genre: '書籍'
  },
  {
    title: '秋新歓の予定決定!!',
    content: '秋新歓に出すコンテンツについて決まりました',
    date: '2020/10/22',
    genre: '新歓'
  },
  {
    title: 'お菓子購入!',
    content: '新たにチョコを購入しました',
    date: '2020/10/23',
    genre: 'お菓子'
  },
  {
    title: 'News3',
    content: 'Wikiの作成が順調です',
    date: '2020/10/24',
    genre: '新歓'
  },
  {
    title: 'News1',
    content: 'ホームページを作成しました',
    date: '2020/10/25',
    genre: '新着状況'
  },
  {
    title: 'News2',
    content: 'code forceに参加しました',
    date: '2020/10/26',
    genre: 'リリース'
  },
  {
    title: 'News3',
    content: 'Wikiの作成が順調です',
    date: '2020/10/27',
    genre: '新歓'
  }
]
const cyima = [
  {
    name: 'News1',
    url: '/image.png'
  },
  {
    name: 'News2',
    url: '/IMG_20201017_185338.jpg'
  },
  {
    name: 'News3',
    url: '/IMG_20191018_163414.jpg'
  }
]

export default {
  data () {
    return {
      slides: cyima,
      newslist: news
    }
  },
  computed: {
    items () {
      return news
    }
  }
}
</script>

<style scoped>
.recipient {
  margin: 13px 20px;
}
@media screen and (max-width: 400px){
  .carousel {
    height: 200px;
  }
}
.news__date {
    margin: 0px 20px 0px 0px;
}
.news__sort {
  margin: 0px 20px 0px 0px;
  font-size: 14px;
  width: 80px;
  background-color: #7B1FA2;
  color: white;
  border-radius:8px;
  text-align: center;
}
.news__sort__content {
  margin: 5px;
  font-family: "YuGothic","Yu Gothic","Meiryo","ヒラギノ角ゴ","sans-serif";
}
.news__title {
    text-decoration: underline;
    text-decoration-color: #FBC02D;
    text-decoration-thickness: 10px;
}
.overview {
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 70vh;
}
.overview__title {
  font-family: 'Courier New', Courier, monospace;
  font-size: 50px;
  color: black;
}
.overview_text {
  font-size: 20px;
  font-family: 'Times New Roman', Times, serif;
  line-height: 40px;
}
@media screen and (max-width: 400px) {
  .overview {
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 100vh;
}
}
.activitie {
  background-color: white;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 70vh;
}
.activity__title {
  font-family: 'Courier New', Courier, monospace;
  font-size: 50px;
  color: black;
}
.activity__text {
  line-height: 40px;
  font-family: 'Times New Roman', Times, serif;
  font-size: 20px;
}
@media screen and (max-width: 400px) {
  .activitie {
  background-color: white;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 100vh;
}
}
.result {
  background-color:whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 70vh;
}
.result__title {
  font-family: 'Courier New', Courier, monospace;
  font-size: 50px;
  color:  black;

}
.result__text {
  line-height: 40px;
  font-family: 'Times New Roman', Times, serif;
  font-size: 20px;
}
@media screen and (max-width: 400px){
  .result {
  background-color:whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 100vh;
}
}
</style>
