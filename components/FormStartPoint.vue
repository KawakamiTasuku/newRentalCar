<template>
     <v-col>
              <v-text-field
                v-model=StartPoint
                label="出発地点"
                hint="車を借りたい地点を入力してください"
                required></v-text-field>
            </v-col>
</template>
<script>
export default {
  name: 'FormStartPoint',
  data: () => ({
      StartPoint:'',
    }),
}
</script>