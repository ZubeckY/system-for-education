<template>
  <div>
    <land-header/>
    <v-carousel cycle
                height="80vh"
                hide-delimiter-background
                :show-arrows="false">

      <v-carousel-item v-for="(slide, i) in slides"
                       :key="i">
        <v-sheet :color="colors[i]"
                 height="100%">
          <v-row class="fill-height"
                 style="align-items: center;
                 justify-content: center;">

            <div style="font-size: 30px;">
               <i>{{ slide }}</i>
            </div>

          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <main>

      <section class="section">
        <v-container>

          <v-card-title class="section-title">
            <i>Что такое "Название"</i>
          </v-card-title>

          <v-card-text style="text-align: center;">
            "Название" - Это продвинутая CMS система, адаптированная под управление и нужды учителя.
            Которая, в первую очередь, не имеет практических аналогов на рынке. В ней собрано всё необходимое, чем бы пользовался учитель или преподаватель,
            ведя свою учебную деятельность
          </v-card-text>

        </v-container>
      </section>

      <section class="section">
        <v-container style="max-width: 1400px; padding-bottom: 60px">

          <v-card-title class="section-title">фыафы</v-card-title>

          <div class="m3">
            <v-row>
              <v-col>
                <v-card>
                  <v-card-title>
                    Доступность
                  </v-card-title>
                  <v-card-text>
                    Наш проект доступен для каждого под свои задачи
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </div>
          <div class="m3">
            <v-row>
              <v-col>
                <v-card>
                  <v-card-title>
                    Понятный интерфейс
                  </v-card-title>
                  <v-card-text>
                    Мы сделали интерфейс настолько интуитивно понятным, чтобы вы могли в нём легко ориентироваться и работать
                  </v-card-text>
                </v-card>
              </v-col>
              <v-col cols="5">
                <v-card>
                  <v-card-title>
                    ss
                  </v-card-title>
                  <v-card-text>
                    ss
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </div>
          <div class="m3">
            <v-row>
              <v-col cols="10">
                <v-card>
                  <v-card-title>
                    вфыа
                  </v-card-title>
                  <v-card-text>
                    фыафы
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </div>

        </v-container>
      </section>

      <section class="section">
        <v-container>
          <v-row>
            <v-col v-for="i in 2" :key="i">
              <v-card height="300">{{i}}</v-card>
            </v-col>
          </v-row>
          <v-card-text style="font-size: 18px; text-align: center">
            Читайте наши новости
            <v-btn text class="link-btn"
                   @click="$router.push('/land/blog/')"
                   color="var(--primary)">
              Здесь
            </v-btn>
          </v-card-text>
        </v-container>
      </section>

    </main>

    <land-footer/>

  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {

  private colors:any = [
    '#cecece',
    '#cecece',
    '#cecece',
  ]

  private slides:any = [
    'Первый текстовый слайд, содержащий ту или иную информацию',
    'Второй слайд, с неменее важной информацией',
    'Третий слайд, тоже важная информация',
  ]

}

</script>
<style>
:root {
  --primary: #3a66cc;
  --section-gray: #ececec;
}

.m3 {margin: 20px}
.container {max-width: 1200px}

.section {padding: 50px}
.section:nth-child(2n) {background: var(--section-gray)}

.link-btn {padding: 0 !important;}
.section-title {justify-content:center; font-size: 30px; font-weight: 700}

</style>
