<template>
    <v-row justify="center">
      <v-expansion-panels accordion>
        <v-expansion-panel
          v-for="(item,i) in 1"
          :key="i"
        >
          <v-expansion-panel-header>拘り検索欄を開く</v-expansion-panel-header>
          <v-expansion-panel-content>
            
            <v-container
            class="px-0"
            fluid
            >
                <v-checkbox
                v-model="slowly"
                :label="`時間をゆっくりに設定する`"
                ></v-checkbox>
            </v-container>
            
            <v-container
            class="px-0"
            fluid
            >
                <v-checkbox
                v-model="littleSlowly"
                :label="`時間を少しゆっくりに設定する`"
                ></v-checkbox>
            </v-container>

            <v-container
            class="px-0"
            fluid
            >
                <v-checkbox
                v-model="cargo"
                :label="`荷物の量が多いに設定する`"
                ></v-checkbox>
            </v-container>            

          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-row>
  </template>

<script>
export default {
  name :'slowly',
  data: () => ({
    slowly:'',
    littleSlowly:'',
    cargo:'',
  }),
}
</script>