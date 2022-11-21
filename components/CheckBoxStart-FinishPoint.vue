<template>
    <v-container
      class="px-0"
      fluid
    >
      <v-checkbox
        v-model="CheckBoxStartFinishPoint"
        :label="`出発地点と返却地点を同じ場所にする`"
      ></v-checkbox>
    </v-container>
  </template>
  <script>
  export default {
    name :'CheckBoxStartFinishPoint',
    data: () => ({
      CheckBoxStartFinishPoint:'',
    }),
}
</script>