<template>
  <v-row class="pa-4">
    <br />
    <v-col>
      <v-img height="450px" width="800px"  :src="img"></v-img>
    </v-col>
    <v-col>
      
      <h3>提供多樣品牌商品線上展售，秉持著以客為尊的精神，提供更多樣化商品，滿足客戶更全面的服務需求。</h3>
    
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      img: "https://img.technews.tw/wp-content/uploads/2021/12/14143550/paper.jpg",
    };
  },
};
</script>
