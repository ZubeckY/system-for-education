<template>
  <div>
    <app-urok-header/>
    <v-container>
      <br>
      <v-card>
        <v-card-title>
          <div>
            <span>Урок</span>
            <span>12412</span>
          </div>
          <v-spacer></v-spacer>
          <div>
            <span>Сегодня:</span>
            <span>{{new Date ().getUTCDate()}}</span>
            <span>/</span>
            <span>{{new Date ().getUTCMonth()}}</span>
          </div>
        </v-card-title>
        <v-divider></v-divider>
        <v-card-text>
          <v-card>
            <v-card-text>

              <template>
                <v-data-table hide-default-footer
                              :headers="studentsDataHeaders"
                              :items="studentsDataBody"
                              :items-per-page="5"
                              class="elevation-1"

                ></v-data-table>
              </template>

            </v-card-text>
          </v-card>

        </v-card-text>
      </v-card>

      <br>

      <app-urok-statistic/>
    </v-container>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private studentsDataHeaders:any = [
    { text: 'Фамилия', value: 'secondName' },
    { text: 'Имя', value: 'firstName' },
    { text: 'Присутствует', value: 'Present' },
    { text: 'Опоздал', value: 'late' },
    { text: 'Время опоздания', value: 'lateTime' },
  ]



}
</script>
