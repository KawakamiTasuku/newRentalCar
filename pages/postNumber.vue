<!--  <template>
    <section class="container">
      <input type="text" placeholder="郵便番号を入力"/>
      <button>住所自動入力</button>
        <p>{{resultData}}</p>
        <p>都道府県：</p>
        <p>住所1：</p>
        <p>住所2：</p>
    </section>
  </template>
  
  <script>
  import axios from 'axios';

  Vue.prototype.$axios = axios;

  /* const axios = require('axios'); */

  let url = 'http://zipcloud.ibsnet.co.jp/api/search?zipcode=';
  
  export default {
    async asyncData() {
      let zipcode = '154-0024';
      let result = await axios.get(url + zipcode);
      return { resultData: result.data.results[0] };
    }
  }
  </script> -->
 

<template>
  <div>
    <div>
      <input type="text" v-model="zipcode" placeholder="郵便番号を入力" />
      <button @click="fetch">検索</button>
    </div>
    <div>{{ result }}</div>
  </div>
</template>

<script>
export default {
  data: () => ({
    zipcode: "",
    result: null,
  }),
  methods: {
    async fetch() {
      const params = { zipcode: this.zipcode };
      const res = await this.$axios.get("/api/search", { params });
      this.result = res.data;
    },
  },
};
</script>