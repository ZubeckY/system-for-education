<template>
  <v-row justify="center">
    <v-dialog v-model="dialogAskToExit"
              max-width="600"
              persistent>

      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on"
               class="app-menu_button">
          Выйти в кабинет
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="text-h5">
          Выйти в кабинет
        </v-card-title>

        <v-card-text>
          <div>
            Вы действительно хотите выйти из кабинета?
          </div>
        </v-card-text>

        <v-card-actions>
          <v-row>
            <v-col class="col-auto">
              <v-btn text
                     @click="dialogAskToExit = false">
                Отмена
              </v-btn>
            </v-col>
            <v-spacer></v-spacer>
            <v-col class="col-auto">
              <v-btn text
                     @click="goBackToMainPage">
                Выйти
              </v-btn>
            </v-col>
          </v-row>
        </v-card-actions>
      </v-card>

    </v-dialog>
  </v-row>
</template>

<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private dialogAskToExit:boolean = false
  goBackToMainPage () {
    this.dialogAskToExit = false
    this.$router.push ('/personal')
  }
}
</script>
