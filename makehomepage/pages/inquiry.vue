<template>
  <v-app>
    <section class="inquiry-top">
      <v-container
        class=""
      >
        <v-row
          class="mb-16 mt-10"
        >
          <v-col>
            <h1 class="text-center">
              プログラミングサークルPabloへのお問い合わせ
            </h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col
            offset-md="3"
            md="7"
          >
            <p>
              お問い合わせはこちらからお送りください。後日担当者よりご連絡させていただきます。必要事項をご記入の上、「入力の確認」
              ボタンをクリックしてください。
            </p>
          </v-col>
        </v-row>
        <v-form
          class="inqury_validation"
        >
          <v-row
            class="mt-10 mb-10"
          >
            <v-col
              offset-md="3"
              md="6"
            >
              <p class="text-h5 title">
                お名前<span class="required pr-1 ml-2">
                  必須
                </span>
              </p>
              <v-text-field
                v-model="client"
                class="mt-3"
                outlined
                :rules="[required]"
              />
            </v-col>
          </v-row>
          <v-row
            class="mt-10 mb-10"
          >
            <v-col
              offset-md="3"
              md="6"
            >
              <p class="text-h5 title">
                メールアドレス<span class="required pr-1 ml-2">
                  必須
                </span>
              </p>
              <v-text-field
                v-model="mail"
                class="mt-3"
                outlined
                label="example@example.com"
                :rules="[mailcheck]"
              />
            </v-col>
          </v-row>
          <v-row
            class="mt-10 mb-10"
          >
            <v-col
              offset-md="3"
              md="6"
            >
              <p class="text-h5 title">
                電話番号<span class="not-required pr-1 ml-2">
                  任意
                </span>
              </p>
              <p>ハイフン(-)ありでお願いします</p>
              <v-text-field
                v-model="pnumber"
                class="mt-3"
                outlined
                label="123-4567-8901"
              />
            </v-col>
          </v-row>
          <v-row
            class="mt-10"
          >
            <v-col
              offset-md="3"
              md="6"
            >
              <p class="text-h5 title">
                お問い合わせ内容<span class="required pr-1 ml-2">
                  必須
                </span>
              </p>
              <v-textarea
                v-model="content"
                class="mt-3"
                outlined
              />
            </v-col>
          </v-row>
          <v-row>
            <v-col
              offset-md="3"
              md="4"
            >
              <v-btn
                rounded
                width="200px"
                color="accent"
                @click="comfirm"
              >
                入力の確認
              </v-btn>
            </v-col>
          </v-row>
          <v-dialog
            v-model="check"
            max-width="400"
          >
            <v-card>
              <v-card-title>入力内容の確認</v-card-title>
              <v-card-text>
                <v-list>
                  <v-list-item-group>
                    <v-list-item>
                      <v-list-item-content>
                        <v-list-item-title>お名前:</v-list-item-title>
                        <v-list-item-subtitle>{{ client }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-content>
                        <v-list-item-title>メールアドレス:</v-list-item-title>
                        <v-list-item-subtitle>{{ mail }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-content>
                        <v-list-item-title>電話番号:</v-list-item-title>
                        <v-list-item-subtitle>{{ pnumber }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-content>
                        <v-list-item-title>お問い合わせ内容:</v-list-item-title>
                        <v-list-item-subtitle>{{ content }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list-item-group>
                </v-list>
                <v-btn
                  rounded
                  color="accent"
                  @click="submit"
                >
                  送信
                </v-btn>
              </v-card-text>
            </v-card>
          </v-dialog>
          <v-dialog
            v-model="fail"
            max-width="290"
          >
            <v-card>
              <v-card-title>入力が間違っています</v-card-title>
              <v-card-text>
                お手数ですが、もう一度入力内容をご確認ください。
              </v-card-text>
            </v-card>
          </v-dialog>
          <v-dialog
            v-model="success"
            max-width="300"
          >
            <v-card>
              <v-card-title>送信に成功しました</v-card-title>
            </v-card>
          </v-dialog>
          <v-snackbar
            v-model="snackbar"
            timeout="5000"
          >
            送信に失敗しました。再度送信してください。
          </v-snackbar>
        </v-form>
      </v-container>
    </section>
  </v-app>
</template>

<script>

export default {
  name: 'Inquiry',
  layout: 'ilayout',
  data () {
    return {
      snackbar: false,
      success: false,
      check: false,
      fail: false,
      client: '',
      pnumber: '',
      mail: '',
      content: '',
      senddata: '',
      required: value => !!value || '必ず入力してください!',
      mailcheck: (mail) => {
        const reg = /^[A-Za-z0-9]{1}[A-Za-z0-9_.-]*@{1}[A-Za-z0-9_.-]{1,}\.[A-Za-z0-9]{1,}$/
        return reg.test(mail)
      }
    }
  },
  methods: {
    lrequired () {
      return !!this.client && !!this.mail
    },
    lmaikcheck () {
      const reg = /^[A-Za-z0-9]{1}[A-Za-z0-9_.-]*@{1}[A-Za-z0-9_.-]{1,}\.[A-Za-z0-9]{1,}$/
      return reg.test(this.mail)
    },
    lphonecheck () {
      const reg1 = /^0\d-\d{4}-\d{4}$/
      const reg2 = /^0\d{3}-\d{2}-\d{4}$/
      const reg3 = /^\(0\d\)\d{4}-\d{4}$/
      const reg4 = /^\(0\d{3}\)\d{2}-\d{4}$/
      const reg5 = /^(070|080|090)-\d{4}-\d{4}$/
      const reg6 = /^050-\d{4}-\d{4}$/
      const reg7 = /^0120-\d{3}-\d{3}$/
      return !this.pnumber || reg1.test(this.pnumber) || reg2.test(this.pnumber) || reg3.test(this.pnumber) ||
      reg4.test(this.pnumber) || reg5.test(this.pnumber) || reg6.test(this.pnumber) || reg7.test(this.pnumber)
    },
    comfirm () {
      if (this.lrequired() && this.lmaikcheck() && this.lphonecheck()) {
        this.check = true
      } else {
        this.fail = true
      }
    },
    async submit () {
      const senddata = 'お名前:' + this.client + '\n' + '電話番号:' + this.pnumber + '\n' + 'メールアドレス:' + this.mail + '\n' + 'お問い合わせ内容:' + '\n' + this.content
      const config = {
        headers: { 'content-type': 'application/x-www-form-urlencoded' }
      }
      const params = new URLSearchParams({
        token: process.env.API_KEY,
        channel: '#お問い合わせ',
        text: senddata
      })
      await this.$axios.$post('https://slack.com/api/chat.postMessage', params, config).then(
        () => {
          this.check = false
          this.success = true
        }
      ).catch(
        () => {
          this.snackbar = true
        }
      )
    }
  }
}
</script>
<style scoped>
.inquiry-top {
  height: 1500px;
  background-color: whitesmoke;
}
.title {
  font-weight: 550;
  font-size: 400px;
}

.required {
  font-size: 15px;
  width: 90px;
  background-color: #D32F2F;
  color: white;
  border-radius:4px;
  text-align: center;
}
.not-required {
  font-size: 15px;
  width: 90px;
  background-color: #388E3C;
  color: white;
  border-radius:4px;
  text-align: center;
}

</style>
