<template>
  <div class="text-center" data-app>
    <v-dialog v-model="lateDialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <span v-if="lateCount === 0">
          Нет
        </span>
        <v-btn v-else v-bind="attrs" v-on="on">
          Показать <span>({{ lateCount }})</span>
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          Список отсутствующих
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
  private lateCount:number = 7
  private lateDialog:boolean = false
  closeMissing () {this.lateDialog = false}
}
</script>
