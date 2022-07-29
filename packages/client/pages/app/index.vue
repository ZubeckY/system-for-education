<template>
  <div class="app-menu" data-app>
    <app-menu/>
    <app-can-i-help/>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator";
@Component
export default class extends Vue {}
</script>
<style>
  .app-menu {
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .app-menu-wrapper {
    max-width: 500px; align-items: center;
    display: flex; width: 100%; height: 350px;
    flex-direction: column; justify-content: center;
  }
  .app-menu_button {
    margin: 15px 10px; width:100vw !important; height:100vh !important;
    max-width: 450px !important; max-height:60px !important;
  }
  .can-i-help {position: absolute;right: 20px;bottom: 20px;}


</style>
