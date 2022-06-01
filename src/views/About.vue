<template>
  <v-row class="pa-4">
    <br />
    <v-col>
      <v-img height="500px" :src="img"></v-img>
    </v-col>
    <v-col>
      <h1>提供您最方便點數交易</h1>
      <h3>雖然沒有華麗的包裝，沒有過多的文字，只抱持著一股堅持，帶給您更便</h3>
      <h3>利的交易模式，是我們唯一的使命。 </h3>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      img: "https://storage.googleapis.com/www-cw-com-tw/article/202102/article-6033500eb90df.jpg",
    };
  },
};
</script>
