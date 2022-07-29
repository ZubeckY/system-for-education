<template>
  <div>
    <land-header/>
    <v-container>
      <div>
        <v-btn href="/app">Перейти в приложение</v-btn>
      </div>
      <div>
        <br>
        <v-card>
          <v-card-title>Личная информация</v-card-title>
          <v-divider></v-divider>
          <v-row>
            <v-col>
              <v-card-text>Ваш Id: </v-card-text>
              <v-card-text>Имя: </v-card-text>
              <v-card-text>Фамилия:</v-card-text>
              <v-card-text>Отчество: </v-card-text>
              <v-card-text>Дата рождения: </v-card-text>
              <v-card-text>Пол: </v-card-text>
              <v-card-text>Место работы: </v-card-text>
              <v-card-text>
                Фотография <span>|_|</span>
                <span v-if="1">
                  <v-btn text
                         color="#002eff">
                    Выбрать
                  </v-btn>
                </span>
                <span v-else>
                  <v-btn text
                         color="#002eff">
                    Изменить
                  </v-btn>
                  <v-btn text
                         color="#FF372DE5">
                    Удалить
                  </v-btn>
                </span>
              </v-card-text>
            </v-col>
          </v-row>
        </v-card>

        <br>

        <v-card>
          <v-card-title>Контактная информация</v-card-title>
          <v-divider></v-divider>
          <v-card-text>Телефон: </v-card-text>
          <v-card-text>E-mail:</v-card-text>
          <v-card-text>Адрес: </v-card-text>
          <v-divider></v-divider>
          <v-card-text>СоцСети</v-card-text>
          <v-divider></v-divider>
          <v-card-text>VK: </v-card-text>
          <v-card-text>Telegram: </v-card-text>
        </v-card>

        <br>

        <v-card>
          <v-card-title>Способ оплаты</v-card-title>
          <v-divider></v-divider>
          <v-card-text>Количество карт: 0</v-card-text>
        </v-card>

        <br>

        <v-card>
          <v-card-title>Информация о приложении</v-card-title>
          <v-divider></v-divider>
          <v-card-text>Подтверждённый аккаунт: Да / нет</v-card-text>
          <v-card-text>Мультиаккаунт : Да / нет</v-card-text>
          <v-divider></v-divider>
          <v-card-text>Тариф: Вид тарифа</v-card-text>
          <v-card-text>Оплата по тарифу: Сумма р.</v-card-text>
          <v-card-text>
            <v-row>
              <v-col>
                <v-text-field label="Купон"
                              clearable/>
              </v-col>
              <v-col>
                <v-btn text
                       color="#002eff">
                  Применить
                </v-btn>
              </v-col>
            </v-row>
          </v-card-text>
          <v-card-text>Статус оплаты: оплачено / нет оплаты</v-card-text>
          <v-card-text>Статус работы: активно / не активно</v-card-text>
          <v-divider></v-divider>
          <v-card-text>Дата начала тарифа: Дата</v-card-text>
          <v-card-text>Дата окончания тарифа: Дата</v-card-text>
          <v-divider></v-divider>
          <v-card-text>Дата регистрации аккаунта: Дата</v-card-text>
        </v-card>

        <br>
        <v-card>
          <v-card-title>Дополнительно</v-card-title>
          <v-divider></v-divider>
          <v-card-text>Статус: Пользователь</v-card-text>
          <v-card-text v-if="1">Админ доступ: Нет</v-card-text>
        </v-card>

        <br>
        <br>

      </div>

    </v-container>
    <land-footer/>
  </div>
</template>
<script lang="ts">
import {Component,  Vue} from "vue-property-decorator";
@Component
export default class extends Vue {
}
</script>
