<template>
  <v-app :class="$style.body">
    <AppBar />

    <v-main   >
        <div :class="$style.main">
        <router-view />
        </div>
    </v-main>

    <footer :class="$style.footer">
      <v-text>電子郵件：&nbsp;red_ocean2021@outlook.com</v-text>
      <br />     
      <v-text>統編：&nbsp;83130599 </v-text>
      <br/>
      <v-text>公司地址：&nbsp;台中市西屯區西屯路二段256巷6號2樓之2</v-text>
       <p>© 2022 Tong-Chen</p>
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
  background-color: #6b778d;
  font-size: 15px;
  color: azure;
  position:fixed;
  bottom: 0;
  width: 100%;
  height: 85px;

  padding-left: 1%;

}

@media (max-width: 768px) {
  .footer {
    display: none;
  }
  
}
</style>
