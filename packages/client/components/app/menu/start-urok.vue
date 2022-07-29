<template>
  <v-row justify="center">
    <v-dialog v-model="dialogStartParamsWindow"
              max-width="600" persistent>

      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on"
               class="app-menu_button">
          Урок
        </v-btn>
      </template>
      <v-card>
        <v-card-title class="text-h5">Начать урок</v-card-title>

        <v-card-text>
          <template>
            <v-card>
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-card-text>

                    <v-select :items="teacherList"
                              label="Выбор учителя"
                              item-text="teacher-name"
                              item-value="teacher-id"
                              outlined>
                    </v-select>
                  </v-card-text>
                </v-window-item>

                <v-window-item :value="2">
                  <v-card-text>

                    <v-select :items="itemsList"
                              label="Выбор предмета"
                              item-text="item-name"
                              item-value="item-id"
                              outlined>
                    </v-select>

                  </v-card-text>
                </v-window-item>

                <v-window-item :value="3">
                  <v-card-text>

                    <v-select :items="areasList"
                              label="Выбор кабинета"
                              item-text="area-name"
                              item-value="area-id"
                              outlined>
                    </v-select>

                  </v-card-text>
                </v-window-item>

              </v-window>

              <v-divider></v-divider>

            </v-card>
          </template>

        </v-card-text>

        <v-card-actions>
          <v-row>
            <v-col class="col-auto">
              <v-btn text
                     @click="backStepOrCloseFunc">
                {{ step === 1 ? 'Отмена' : 'Назад'}}
              </v-btn>
            </v-col>
            <v-spacer></v-spacer>
            <v-col class="col-auto">
              <v-btn text
                     :disabled="stepDisabled"
                     @click="forwardStepOrCloseFunc">
                {{ step === 3 ? 'Начать' : 'Далее'}}
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
  private dialogStartParamsWindow:boolean = false
  private stepDisabled:boolean =  false

  private step:number = 1;

  private teacherList:any = [
    {
      'teacher-id': '1',
      'teacher-name': 'Имя',
    }
  ]

  private itemsList:any = [
    {
      'item-id': '1',
      'item-name': 'Русский',
    }
  ]

  private areasList:any = [
    {
      'area-id': '1',
      'area-name': '12 кабинет',
    }
  ]

  backStepOrCloseFunc () {
    this.step == 1 ? this.dialogStartParamsWindow = false : this.step --
  }
  forwardStepOrCloseFunc () {
    if (this.step == 3 ) {
      this.$router.push('/app/workspace')
    } else {
      this.step ++
    }
  }
}

</script>
