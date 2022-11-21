<template>
    <v-row justify="space-around">
      <v-date-picker
        v-model="dates"
        :show-current="false"
        range
      ></v-date-picker>
    </v-row>
  </template>

<script>
  export default {
    data () {

      return {
        dates:[(new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),(new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000 + 7 * 24 * 60 * 60000 )).toISOString().substr(0, 10)],
        /* date1: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),
        date2: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000) + 7 * 24 * 60 * 60000).toISOString().substr(0, 10), */
    }
  },
}
</script>