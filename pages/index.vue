<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <!-- //welcomeページで出てくるロゴ2つ -->
      <!-- <v-card class="logo py-4 d-flex justify-center">
        <NuxtLogo />
        <VuetifyLogo />
      </v-card> -->
      <!-- //welcomページで一番最初に出てくるカード -->
      <v-card>
        <v-card-title class="demo">
          出発・到着地点、出発日時到着日時を入力してください
        </v-card-title>
      </v-card>
      <v-form v-model="valid">
        <v-row>
          <FormStartPoint />
        </v-row>

        <v-row>
          <FormDestination />
        </v-row>  

        <v-row>
          <FormFinishPoint />
        </v-row>
      </v-form>
        <CheckBoxStartFinishPoint />
        <Searchoption />
        <DatePickerStartFinishDay />
        <!--       <v-btn
        color="primary"
        elevation="2"
      >出発地点と同じ地点に返却する
      </v-btn> -->
<!--       <v-form v-model="valid">
        <v-row>
          <v-col>
              <v-text-field
                v-model=出発日時
                label="出発日時"
                hint="車を借りはじめたい日時を入力してください"
                required></v-text-field>
          </v-col>
        </v-row>
      </v-form> -->
<!--         model: {{ dates }}
        {{dayStart}}
        </v-col>  -->
<!--       <v-form v-model="valid">
        <v-row>
          <v-col>
              <v-text-field
                v-model=返却日時
                label="返却日時"
                hint="車を返したい日時を入力してください"
                required></v-text-field>
          </v-col>
        </v-row>
      </v-form> -->

       <v-card>
        <!-- //カードの見出し -->
        <!-- <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title> -->
        <!-- //カードの本文 -->
        <!-- <v-card-text>
          <p>Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
          <p>
            For more information on Vuetify, check out the <a
              href="https://vuetifyjs.com"
              target="_blank"
              rel="noopener noreferrer"
            >
              documentation
            </a>.
          </p>
          <p>
            If you have questions, please join the official <a
              href="https://chat.vuetifyjs.com/"
              target="_blank"
              rel="noopener noreferrer"
              title="chat"
            >
              discord
            </a>.
          </p>
          <p>
            Find a bug? Report it on the github <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              rel="noopener noreferrer"
              title="contribute"
            >
              issue board
            </a>.
          </p>
          <p>Thank you for developing with Vuetify and I look forward to bringing more exciting features in the future.</p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
          <hr class="my-3">
          <a
            href="https://nuxtjs.org/"
            target="_blank"
            rel="noopener noreferrer"
          >
            Nuxt Documentation
          </a>
          <br>
          <a
            href="https://github.com/nuxt/nuxt.js"
            target="_blank"
            rel="noopener noreferrer"
          >
            Nuxt GitHub
          </a>
        </v-card-text> -->
        <!-- //continueのボタン -->
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            検索する
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import CheckBoxStartFinishPoint from '../components/CheckBoxStart-FinishPoint.vue';
import DatePickerStartFinishDay from '../components/DatePickerStartFinishDay.vue';
import FormDestination from '../components/FormDestination.vue';
import FormFinishPoint from '../components/FormFinishPoint.vue';
import FormStartPoint from '../components/FormStartPoint.vue';
import Searchoption from '../components/Searchoption.vue';


export default {
    name: "IndexPage",
    components: { DatePickerStartFinishDay, Searchoption }
}
    components: { FormStartPoint, FormDestination, FormFinishPoint, CheckBoxStartFinishPoint }
</script>
