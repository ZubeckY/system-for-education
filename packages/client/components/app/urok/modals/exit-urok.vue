<template>
  <div class="text-center" data-app>
    <v-dialog v-model="exitDialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on">
          Завершить урок
        </v-btn>
      </template>
      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
          Завершение урока
        </v-card-title>
        <v-card-text>
          Вы действительно хотите завершить урок прямо сейчас?
        </v-card-text>
        <v-card-actions>
          <v-btn text @click="exitDialog = false">Отмена</v-btn>
          <v-spacer></v-spacer>
          <app-urok-modals-exit-urok-ok/>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private exitDialog:boolean = false
}
</script>
