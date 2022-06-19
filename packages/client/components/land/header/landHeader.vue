<template>
  <header>
    <v-card>
      <v-container>
        <v-row>
          <v-col>
            <v-card-text>
              <v-btn text @click="$router.push('/')">LOGO</v-btn>
            </v-card-text>
          </v-col>
          <v-spacer></v-spacer>
          <v-col v-for="(item, i) in items" :key="i" cols="auto">
            <v-card-text>
              <v-btn text @click="$router.push(item.link)">
                {{ item.title }}
              </v-btn>
            </v-card-text>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </header>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private items:any = [
    {
      link: '/land/about-us',
      title: 'О нас',
    },
    {
      link: '/land/about-project',
      title: 'О проекте',
    },
    {
      link: '/personal',
      title: 'Кабинет',
    },
    {
      link: '/tz',
      title: 'ТЗ',
    },
  ]
}
</script>
<style>.container {max-width: 1200px}</style>
