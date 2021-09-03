<template>
  <v-app>
     <AppBar/>

    <v-main class="grey lighten-3">
      <router-view/>
    </v-main>

  <footer  :class="$style.footer">
   <v-text>電子郵件： useepays@gmail.com</v-text>
   <br>
   <v-text>電話號碼： +886-981-280-323</v-text>
    <!-- A footer for the page. -->
  </footer>
  </v-app>
</template>

<script>
import AppBar from '../src/components/AppBar.vue'
export default {
  name: 'App',
  components:{
    AppBar
  },
  data: () => ({
    //
  }),
};
</script>
<style module>
.footer{
  
   background-color: #333;
   height: 80px;
   margin-top: 20px;
   color: azure;
  
}
</style>
