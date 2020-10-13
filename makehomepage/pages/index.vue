<template>
<v-app>
<v-container >
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
  </v-container>
<v-container fluid>
  <v-parallax
    src="/pablo.png"> <!--https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg-->
    <v-row
      align="start"
      justify="center">
      <v-col
        cols="12">
        <h1>サークル概要</h1>
        <h2></h2>
        <p>プログラミングサークルPabloは神戸を拠点に活動しています。</p>
        </v-col></v-row>

  </v-parallax>
  </v-container>

<v-container fluid>
  <v-parallax
    src="/pablo.png">
    <v-row
      align="start"
      justify="center">
      <v-col
        cols="12">
        <h1>活動内容</h1>
        <h2>主に次のような活動をしています</h2>
        <p></p>
        </v-col></v-row>

  </v-parallax>
  </v-container>

<v-container fluid>
  <v-parallax
    src="/pablo.png">
    <v-row
      align="start"
      justify="center">
      <v-col
        cols="12">
        <h1>活動成果!!</h1>
        <h4></h4>
        </v-col></v-row>

  </v-parallax>
</v-container>
</v-app>
</template>

<script>
const cyima = [
  {
    name: '活動内容1',
    url: '/1.png'
  },
  {
    name: '活動内容2',
    url: '/2.png'
  },
  {
    name: '活動内容3',
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
.v-toolbar__title{
  overflow: visible;
  margin: 50px;

}
</style>
