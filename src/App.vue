<template>
  <v-app :class="$style.body">
    <AppBar />

    <v-main class="blue-grey lighten-2"  >
        <div :class="$style.main">
        <router-view />
        </div>
    </v-main>

    <footer :class="$style.footer">
      <v-text>電子郵件：&nbsp;hogsheng@gmail.com</v-text>
      <br />
      <v-text>電話號碼：&nbsp;0986-830051 &nbsp;</v-text>
     
      <v-text>統編：&nbsp;42898323 </v-text>
      <br/>
      <v-text>公司地址：&nbsp;台中市南屯區五權西路二段666號6樓之4</v-text>
       <p>© 2021 Hong Sheng</p>
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
  height: 100%;
  margin: 0;
  width: 100%;
}
.main{
  padding-bottom: 50px; 

}
.footer {
  background-color: #333;
  font-size: 15px;
  color: azure;
  position:fixed;
  bottom: 0;
  width: 100%;

  padding-left: 1%;

}

@media (max-width: 768px) {
  .footer {
    display: none;
  }
  
}
</style>
