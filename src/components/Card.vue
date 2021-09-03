<template>
<div    class="d-flex justify-start mb-6">
  
  <v-card
    :loading="loading"
    max-width="25%"
    v-for="item in data" :key="item"
  >
   

    <v-img
   
      max-width="100%"
      :src="item.img"
    ></v-img>

    <v-card-title>{{item.name}}</v-card-title>

    <v-card-text>
        {{item.price}}
    </v-card-text>


  
  </v-card>
 </div>
</template>
<script>

export default {
props: {
    data:Array,
},
}
</script>