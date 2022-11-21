<template>
    <v-col>
        <v-text-field
        v-model=Destination
        label="目的地点"
        hint="今回行きたい場所を入力してください"
        required></v-text-field>
    </v-col>
</template>
<script>
export default {
  name: 'FormDestination',
  data: () => ({
      Destination:'',
    }),
}
</script>