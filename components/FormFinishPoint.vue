<template>
    <v-col>
        <v-text-field
        v-model=FinishPoint
        label="返却地点"
        hint="車を返す地点を入力してください"
        required></v-text-field>
    </v-col>
</template>
<script>
export default {
  name: 'FormFinishPoint',
  data: () => ({
      FinishPoint:'',
    }),
}
</script>