/* eslint-disable vue/html-indent */
<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12" md="6" xs="12">
          <v-carousel
            cycle
            height="400"
            hide-delimiter-background
            show-arrows-on-hover
          >
            <v-carousel-item v-for="(slide, i) in slides" :key="i">
              <v-sheet :color="colors[i]" height="100%">
                <v-row class="fill-height" align="center" justify="center">
                  <div class="display-3">
                    {{ slide }} Slide
                  </div>
                </v-row>
              </v-sheet>
            </v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>
    </v-container>
    <section class="overview" href="#">
      <v-container fill-height pt-16 pb-16>
        <div class="text-h2 text-center">
          <span
            class="result__title"
          >神戸大学2回生 Y.K</span>
        </div>
        <hr color="#FBC02D">

        <v-row>
          <v-col cols="12" md="7" xs="12">
            <v-card>
              <v-img src="/yoshihiro.jpg" />
            </v-card>
          </v-col>
          <v-col cols="12" md="5" xs="12">
            <v-virtual-scroll
              :items="items"
              height="350"
              item-height="70"
            >
              <template v-slot="{ item }">
                <v-list-item>
                  <p class="">
                    {{ item.date }}
                  </p>
                  <v-list-item-action>
                    <div class="">
                      <p class="">
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
          </v-col>
        </v-row>
      </v-container>
    </section>

    <v-col
      align-self="center"
      justify="end"
    >
      <section class="activitie" href="#">
        <v-container class="activitie" fill-height pt-16 pb-16>
          <v-row>
            <v-col cols="12" md="7" xs="12">
              <v-card>
                <v-img src="/Ryouzen.jpg" />
              </v-card>
            </v-col>
            <v-col cols="12" md="5" xs="12">
              <div class="text-h2 text-center">
                <span
                  class="result__title"
                ><p>神戸大学 1回生</p><p> 文学部 R.N</p></span>
              </div>
              <hr color="#FBC02D">
              <template>
                <v-card
                  class="mx-auto"
                  max-width="500"
                  cols="offset-6"
                >
                  <v-toolbar
                    color="#FBC02D"
                    dark
                  >
                    <v-toolbar-title>実績</v-toolbar-title>

                    <v-spacer />
                  </v-toolbar>

                  <v-list two-line>
                    <v-list-item-group
                      v-model="selected"
                      active-class="pink--text"
                      multiple
                    >
                      <template v-for="(item, index) in items">
                        <v-list-item :key="item.title">
                          <template v-slot:default="{ active }">
                            <v-list-item-content>
                              <v-list-item-title v-text="item.title" />

                              <v-list-item-subtitle
                                class="text--primary"
                                v-text="item.headline"
                              />

                              <v-list-item-subtitle v-text="item.subtitle" />
                            </v-list-item-content>

                            <v-list-item-action>
                              <v-list-item-action-text v-text="item.action" />

                              <v-icon
                                v-if="!active"
                                color="grey lighten-1"
                              >
                                mdi-star-outline
                              </v-icon>

                              <v-icon
                                v-else
                                color="yellow darken-3"
                              >
                                mdi-star
                              </v-icon>
                            </v-list-item-action>
                          </template>
                        </v-list-item>

                        <v-divider
                          v-if="index < items.length - 1"
                          :key="index"
                        />
                      </template>
                    </v-list-item-group>
                  </v-list>
                </v-card>
              </template>
            </v-col>
          </v-row>
        </v-container>
      </section>
    </v-col>
    <section class="result" href="#">
      <v-container fill-height pt-16 pb-16>
        <v-row>
          <v-col cols="12" md="7" xs="12">
            <v-card>
              <v-img src="/takurou.jpg" />
            </v-card>
          </v-col>
          <v-col cols="12" md="5" xs="12">
            <div class="text-h2 text-center">
              <span
                class="result__title"
              >競技プログラミングを驚異の速さで習得中</span>
            </div>
            <hr color="#FBC02D">
            <p class="result__text">
              神戸大学 2回生 小山 よしひろ
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
  name: 'Top',
  data () {
    return {
      slides: cyima
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
@media screen and (max-width: 400px) {
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
  background-color: #7b1fa2;
  color: white;
  border-radius: 8px;
  text-align: center;
}
.news__sort__content {
  margin: 5px;
  font-family: "YuGothic", "Yu Gothic", "Meiryo", "ヒラギノ角ゴ", "sans-serif";
}
.news__title {
  text-decoration: underline;
  text-decoration-color: #fbc02d;
  text-decoration-thickness: 10px;
}
.overview {
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
}
.overview__title {
  font-family: "Courier New", Courier, monospace;
  font-size: 30px;
  color: black;
}
.overview_text {
  font-size: 20px;
  font-family: "Times New Roman", Times, serif;
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
  font-family: "Courier New", Courier, monospace;
  font-size: 50px;
  color: black;
}
.activity__text {
  line-height: 40px;
  font-family: "Times New Roman", Times, serif;
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
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
}
.result__title {
  font-family: "Courier New", Courier, monospace;
  font-size: 50px;
  color: black;
}
.result__text {
  line-height: 40px;
  font-family: "Times New Roman", Times, serif;
  font-size: 20px;
}
@media screen and (max-width: 400px) {
  .result {
    background-color: whitesmoke;
    background-size: cover;
    background-position: center center;
    width: 100%;
    height: 100vh;
  }
}
</style>
