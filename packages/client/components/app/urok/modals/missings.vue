<template>
  <div class="text-center" data-app>
    <v-dialog v-model="missingDialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <span v-if="missingCount === 0">
          Нет
        </span>
        <v-btn v-else v-bind="attrs" v-on="on">
          Показать <span>({{ missingCount }})</span>
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          Список опоздавших
        </v-card-title>
        <v-card-text>


        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn text @click="closeMissing">ОК</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private missingCount:number = 5
  private missingDialog:boolean = false
  closeMissing () {this.missingDialog = false}
}
</script>
