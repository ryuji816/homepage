<template>
  <v-app>
    <section class="odd">
      <v-container
        class="mokumoku"
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
            <v-card>
              <v-img src="/IMG_20201020_193746.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="artitle">もくもく会</span>
            </div>
            <hr class="primary" color="primary">
            <p class="text-justify content text">
              もくもく会とは主にプログラミングなどの作業・勉強などをする目的で複数人が集まり、"黙々と"作業をするイベントです。 集まって作業することで集中して作業ができ、困ったら相談するなどして効率的な作業や勉強が行えます。そして最後にはその日行った作業や勉強内容を各人が共有することで知見を広げたり、発表や質疑応答を通して自分自身の理解を深めることができます。
            </p>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="even">
      <v-container
        class="competitive-programming"
        fill-height
        pt-16
        pb-16
      >
        <v-row>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="artitle">競技プログラミング振り返り会</span>
            </div>
            <hr class="primary" color="primary">
            <p class="text-justify content text">
              毎週末に開催されるAtCoderなどの競技プログラミングのコンテストの振り返りを行います。Pabloには競技プログラミングに参加しているメンバーが多数在籍しており、コンテスト結果の共有・解けなかった問題の復習などを行っています。
            </p>
          </v-col>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card>
              <v-img src="/IMG_20201020_193746.jpg" />
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="odd">
      <v-container
        class="voluntary-seminar"
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
            <v-card>
              <v-img src="/IMG_20201020_193746.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="artitle">自主ゼミ</span>
            </div>
            <hr class="primary" color="primary">
            <p class="text-justify content text">
              Pabloでは有志自主ゼミを開催しています。プログラミングだけではなく、数学など多岐にわたる分野の勉強を行っています。1人では勉強しにくい文献の少ない分野についても、仲間と楽しく勉強することができます。
            </p>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="even">
      <v-container
        class="contract-based-development"
        fill-height
        pt-16
        pb-16
      >
        <v-row>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="artitle">受託開発</span>
            </div>
            <hr class="primary" color="primary">
            <p class="text-justify content text">
              お客様の思い描くサービスを具体的な形にする開発を行っています。特に大学生の方などからご相談をいただく事が多いです。熱い志を持った方のプロジェクトを全力でサポートします。
            </p>
          </v-col>
          <v-col
            cols="12"
            md="7"
            xs="12"
          >
            <v-card>
              <v-img src="/IMG_20201020_193746.jpg" />
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="odd">
      <v-container
        class="in-house-development"
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
            <v-card>
              <v-img src="/IMG_20201020_193746.jpg" />
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            xs="12"
          >
            <div class="text-h2 text-center">
              <span class="artitle">自社開発</span>
            </div>
            <hr class="primary" color="primary">
            <p class="text-justify content text">
              メンバーが考えた企画を具体的なサービスにする活動を行っています。企画からシステム開発、営業まで全てサークル内で行います。
            </p>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </v-app>
</template>

<script>
export default {
  name: 'Activity',
  layout: 'lactivity'
}
</script>
<style scoped>
.odd {
  background-color: white;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 830px;
}
.even {
  background-color: whitesmoke;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 830px;
}
.artitle {
  font-family: 'Courier New', Courier, monospace;
  font-size: 50px;
  color: black;
}
.text {
  line-height: 40px;
  font-family: 'Times New Roman', Times, serif;
  font-size: 20px;
}
</style>
