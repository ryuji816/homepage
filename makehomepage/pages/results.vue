<template>
  <v-app>
    <v-container>
      <v-row>
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
      </v-row>
    </v-container>
    <section class="overview">
      <v-container
        fill-height
        pt-10
        pb-10
      >
        <v-row>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card
              class="pa-3"
              color="#f5f5f5"
            >
              <v-img src="/ryuji.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h3 text-center">
              <span class="overview__title">Performance</span>
            </div>
            <hr color="#FBC02D">
            <v-virtual-scroll
              :items="items"
              height="300"
              item-height="70"
              class="mt-9 mb-9"
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
            <template>
              <v-card
                class="mx-auto pa-5"
                max-width="500"
                cols="offset-6"
                color="#CDCDCD"
                dark
                height="200"
              >
                <v-card-tittle
                  class="text-h5"
                >
                  神戸大学 理学部 R.K
                </v-card-tittle>
                <v-card-subtitle>
                  趣味 読書
                </v-card-subtitle>
              </v-card>
            </template>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="activitie">
      <v-container
        fill-height
        pt-16
        pb-16
      >
        <v-row>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card
              class="pa-3"
            >
              <v-img src="/yoshihiro.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h3 text-center">
              <span class="overview__title">Performance</span>
            </div>
            <hr color="#FBC02D">
            <v-virtual-scroll
              :items="items"
              height="300"
              item-height="70"
              class="mt-9 mb-9"
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
            <template>
              <v-card
                class="mx-auto pa-5"
                max-width="500"
                cols="offset-6"
                color="#CDCDCD"
                dark
                height="200"
              >
                <v-card-tittle
                  class="text-h5"
                >
                  神戸大学 農学部 Y.K
                </v-card-tittle>
                <v-card-subtitle>
                  趣味 音楽
                </v-card-subtitle>
              </v-card>
            </template>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="overview">
      <v-container
        fill-height
        pt-16
        pb-16
      >
        <v-row>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card
              class="pa-3"
              color="#f5f5f5"
            >
              <v-img src="/yukina.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h3 text-center">
              <span class="overview__title">Performance</span>
            </div>
            <hr color="#FBC02D">
            <v-virtual-scroll
              :items="items"
              height="300"
              item-height="70"
              class="mt-9 mb-9"
            >
              <template v-slot="{ item }">
                <v-list-item color="#FFFFFF">
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
            <template>
              <v-card
                class="mx-auto pa-5"
                max-width="500"
                cols="offset-6"
                color="#CDCDCD"
                dark
                height="200"
              >
                <v-card-tittle
                  class="text-h5"
                >
                  神戸大学 文学部 Y.N
                </v-card-tittle>
                <v-card-subtitle>
                  趣味 競技プログラミング
                </v-card-subtitle>
              </v-card>
            </template>
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
  name: 'Top',
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
.bg-white {
  background-color: white;
}
</style>
