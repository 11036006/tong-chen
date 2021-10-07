<template>
  <v-row class="pa-4">
    <br />
    <v-col>
      <v-img max-widh="50%" :src="img"></v-img>
    </v-col>
    <v-col>
      <h1>提供您最頂鮮的食材</h1>
      <h3>雖然沒有華麗的包裝，沒有過多的文字，只抱持著一股堅持，</h3>
      <h3>帶給您平價的消費，新鮮的食材，高檔的享受是我們唯一的使命。</h3>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      img: "http://n.sinaimg.cn/translate/273/w600h473/20180905/Ffn_-hitesuy7663033.jpg",
    };
  },
};
</script>
