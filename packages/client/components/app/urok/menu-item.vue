<template>
  <div class="text-center" data-app>
    <v-dialog v-model="workMenuDialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on">Меню</v-btn>
      </template>

      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
          <span>Меню</span>
          <v-spacer></v-spacer>
          <v-btn text @click="workMenuDialog = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text>
          <v-card-text>
            <v-btn>кнопка</v-btn>
            <v-btn>кнопка</v-btn>
            <v-btn @click="$router.push('/app')">В главное меню</v-btn>
            <app-urok-modals-exit-urok/>
          </v-card-text>
        </v-card-text>

      </v-card>
    </v-dialog>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private workMenuDialog:boolean = false
}
</script>
