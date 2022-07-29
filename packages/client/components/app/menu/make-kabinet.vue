<template>
  <v-row justify="center">

    <v-dialog v-model="dialogAreaWindows"
              fullscreen
              hide-overlay
              transition="dialog-bottom-transition">

      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on"
               class="app-menu_button">
          Кабинет
        </v-btn>
      </template>

      <v-card>
        <v-toolbar>
          <v-spacer></v-spacer>
          <v-btn icon
                 @click="dialogAreaWindows = false">
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
  private dialogAreaWindows:boolean = false
}
</script>

