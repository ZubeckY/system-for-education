<template>
  <v-footer padless
            color="#333"
            style="color: #b4aeae; padding: 20px 0 40px 0">
    <v-row no-gutters
           style="justify-content:center;">
      <v-btn v-for="(item, i) in links" :key="i"
             @click="$router.push(item.link)"
             color="#fff" text
             class="my-2"
             style="margin: 30px 10px; padding: 0">
          {{ item.title }}
      </v-btn>
      <v-col cols="12"
             style="text-align: center"
             class="lighten-2 py-4">
        {{ new Date().getFullYear() }} — <strong>Logo</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
  private links:any = [
    {
      link: '/land/about-us',
      title: 'О нас',
    },
    {
      link: '/land/offer',
      title: 'Информация',
    },
    {
      link: '/land/blog',
      title: 'Блог',
    },
    // {
    //   link: '/land/services',
    //   title: 'Услуги',
    // },
    {
      link: '/land/confidentiality',
      title: 'Кондифициальность',
    },
    {
      link: '/land/contact',
      title: 'Контакты',
    },
  ]

}
</script>
<style>.container {max-width: 1200px}</style>
