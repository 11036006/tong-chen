<template>
<div class="d-flex flex-wrap" >
  
  <v-card
    
    width="260px"
    height="400px"
    style="margin:10px"
    v-for="item in data" :key="item.id"
    :to="{
          name: 'Product',
          params: { data:{id: item.id , name:item.name ,img:item.img,price:item.price}},
     }"
  >
   

    <v-img
      :src="item.img"
      height="250"
    ></v-img>

    <v-card-title>{{item.name}}</v-card-title>

    <v-card-text >
        {{item.price}}元
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