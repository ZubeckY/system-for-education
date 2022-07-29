<template>
  <v-row justify="center">

    <v-dialog v-model="dialogParamsWindows"
              fullscreen
              hide-overlay
              transition="dialog-bottom-transition">

      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on"
               class="app-menu_button">
          Настройки
        </v-btn>
      </template>

      <v-card>
        <v-toolbar>
          <v-spacer></v-spacer>
          <v-btn icon
                 @click="dialogParamsWindows = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-toolbar>
      </v-card>

    </v-dialog>
  </v-row>
</template>
<script lang="ts">
import {Component,  Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private dialogParamsWindows:boolean = false
}
</script>
