<template>
  <div style="background: #fafafa;">
    <v-container class="app-urok-header">
      <v-row class="align-center">
        <v-col>
          <span>Вы: </span>
          <span>Анатольевна А.А.</span>
        </v-col>
        <v-col>
          <span>Предмет: </span>
          <span>Русский Язык</span>
        </v-col>
        <v-col>
          <span>Время:</span>
          <span>{{ HOURS }} : {{ MINUTES }} : {{ SECONDS}} </span>
        </v-col>
        <v-spacer></v-spacer>
        <v-col class="col-auto">
          <app-urok-menu-item/>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {

  /**
   * Пропсами получается следующая информация:
   * - Фамилия Имя Отчество текущего преподавателя
   * - Текущий предмет
 */

  private HOURS:number   = new Date().getHours();
  private MINUTES:number = new Date ().getMinutes()
  private SECONDS:number = new Date ().getSeconds()

  // Таймер
  created () {
    setInterval (()=> {
      this.HOURS   = new Date().getHours();
      this.MINUTES = new Date ().getMinutes()
      this.SECONDS = new Date ().getSeconds()
    }, 1000)
  }
}
</script>
<style>
.app-urok-header {padding: 30px 40px;}
.app-urok-text-button {
  height: 0; font-size: 16px !important;
  text-transform: lowercase; letter-spacing: inherit;
}
.align-center   {align-items: center;}
.justify-center {justify-content: center;}
</style>
