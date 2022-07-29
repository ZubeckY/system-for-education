<template>
  <v-row justify="center">
    <v-dialog v-model="uDoExitDialog"
              persistent max-width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn @click="uDoExitDialog = true">Завершить</v-btn>
      </template>
      <v-card>
        <v-card-title class="text-h5">Вы завершили урок</v-card-title>
        <br>
        <v-card-text>Урок завершён успешно и сохранён!</v-card-text>
        <v-card-text>Для отчётности, его можно найти по следующему пути:</v-card-text>
        <v-card-text>"Меню > Журнал > Проведённые уроки > Номер"</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn text @click="closeUDoExitDialog">ОК</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private uDoExitDialog:boolean = false;
  closeUDoExitDialog () {
    this.uDoExitDialog = false;
    this.$router.push('/app')
  }
}
</script>
