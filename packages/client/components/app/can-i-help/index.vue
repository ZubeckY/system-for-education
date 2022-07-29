<template>
  <v-card class="can-i-help" v-show="canIHelpU">
    <div class="can-i-help-wrapper">
      <v-row>
        <v-col>
          <v-card-title>Есть вопросы?</v-card-title>
        </v-col>
        <v-spacer></v-spacer>
        <v-col class="col-auto">
          <v-btn icon @click="canIHelpU = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-card-text>
        <v-btn class="app-urok-text-button" color="#3aa66c" text>напишите нам</v-btn>
        <span>или пройдите</span>
        <v-btn class="app-urok-text-button" color="#3aa66c" text>режим обучения</v-btn>
      </v-card-text>
    </div>
  </v-card>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private canIHelpU:boolean = true
}
</script>
