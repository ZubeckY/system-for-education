<template>
  <v-expansion-panels>
    <v-expansion-panel>
      <v-expansion-panel-header>
        <v-card-title style="padding: 0">Информация по уроку</v-card-title>
      </v-expansion-panel-header>
      <v-expansion-panel-content>

        <v-row>
          <v-col><v-divider></v-divider></v-col>
        </v-row>

        <v-row>
          <v-col>Преподаёт</v-col>
          <v-col>Анатольевна А.А.</v-col>
        </v-row>

        <v-row>
          <v-col>Предмет</v-col>
          <v-col>Русский Язык</v-col>
        </v-row>

        <v-row>
          <v-col>Кабинет</v-col>
          <v-col>12 кабинет</v-col>
        </v-row>

        <v-row>
          <v-col>Класс/группа</v-col>
          <v-col>9</v-col>
        </v-row>

        <v-row>
          <v-col>Количество по списку</v-col>
          <v-col>24</v-col>
        </v-row>

        <v-row>
          <v-col>Присутствуют</v-col>
          <v-col>17</v-col>
        </v-row>

        <v-row>
          <v-col>Отсутствуют</v-col>
          <v-col>
            <app-urok-modals-missings/>
          </v-col>
        </v-row>

        <v-row>
          <v-col>Опоздали</v-col>
          <v-col>
            <app-urok-modals-latecomers/>
          </v-col>
        </v-row>

        <v-row>
          <v-col><v-divider></v-divider></v-col>
        </v-row>

        <v-row>
          <v-col>Время начала</v-col>
          <v-col>16:00</v-col>
        </v-row>

        <v-row>
          <v-col>Время окончания</v-col>
          <v-col>16:40</v-col>
        </v-row>

        <v-row>
          <v-col>Другое время оконч.</v-col>
          <v-col>
            <v-btn>Поставить</v-btn>
          </v-col>
        </v-row>

      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>

<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  /**
   * Пропсами получается следующая информация:
   * - Фамилия Имя Отчество текущего преподавателя
   * - Текущий предмет
   * - Время начала урока
   * - Время окончания урока
   * - Текущий кабинет
   * - Текущая Класс/группа
   * - Кол-во человек в Класс/группа
   * - Кол-во присутствующих
   * - Кол-во отсутствующих
  */
}
</script>
