<template>
  <v-app :class="$style.body">
    <AppBar />

    <v-main class="blue-grey lighten-2" >
        <div :class="$style.main">
        <router-view />
        </div>
    </v-main>

    <footer :class="$style.footer">
      <v-text>電子郵件： useepays@gmail.com</v-text>
      <br />
      <v-text>電話號碼： +886-981-280-323</v-text>
      <!-- A footer for the page. -->
    </footer>
  </v-app>
</template>

<script>
import AppBar from "../src/components/AppBar.vue";
export default {
  name: "App",
  components: {
    AppBar,
  },
  data: () => ({
    //
  }),
};
</script>
<style module>
.body{
  height: 100%; /*外層高度100%*/
  margin: 0;
  width: 100%;
}
.main{
  padding-bottom: 50px; 
}
.footer {
  background-color: #333;
  height: 80px;
  color: azure;
  position: absolute;
  bottom: 0;
  width: 100%;

}
</style>
