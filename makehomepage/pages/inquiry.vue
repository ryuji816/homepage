<template>
  <v-app>
    <section class="inquiry-top">
    <v-container
      class="">
      <v-row
        class="mb-16 mt-10">
        <v-col>
          <h1 class="text-center">プログラミングサークルPabloへのお問い合わせ</h1>
        </v-col>
        </v-row>
        <v-row>
        <v-col
          offset-md="3"
          md="7"
          >
          <p class="">お問い合わせはこちらからお送りください。後日担当者よりご連絡させていただきます。必要事項をご記入の上、「入力の確認」
            ボタンをクリックしてください。
          </p>
        </v-col>
        </v-row>
          <v-row
            class="mt-10 mb-10">
            <v-col
              offset-md="3"
              md="6">
              <h1>お名前</h1>
              <v-text-field
                class="mt-3"
                v-model="name"
                outlined>
              </v-text-field>
            </v-col>
          </v-row>
          <v-row
            class="mt-10 mb-10">
            <v-col
              offset-md="3"
              md="6">
              <h1>メールアドレス</h1>
              <v-text-field
                class="mt-3"
                v-model="mail"
                outlined>
              </v-text-field>
            </v-col>
          </v-row>
          <v-row
            class="mt-10 mb-10">
            <v-col
              offset-md="3"
              md="6">
              <h1>電話番号</h1>
              <v-text-field
                class="mt-3"
                v-model="phonenumber"
                outlined>
              </v-text-field>
            </v-col>
          </v-row>
          <v-row
            class="mt-10">
            <v-col
              offset-md="3"
              md="6">
              <h1>お問い合わせ内容</h1>
            <v-textarea
              class="mt-3"
              v-model="content"
              outlined>
            </v-textarea>
            </v-col>
          </v-row>
          <v-row>
            <v-col
              offset-md="3"
              md="4">
              <v-btn
            rounded
            width="200px"
            color="accent">
            入力の確認
          </v-btn>
            </v-col>
          </v-row>
    </v-container>
    </section>
  </v-app>
</template>

<script>
export default {
  name: 'Inquiry',
  layout: 'ilayout'
}
</script>
<style scoped>
.inquiry-top {
  height: 180vh;
  background-color: whitesmoke;
}

</style>
