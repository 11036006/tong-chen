<template>
<div class="d-flex flex-wrap" >
  
  <v-card
    
    max-width="200px"
    max-height="400px"
    v-for="item in data" :key="item.id"
    :to="{
          name: 'Product',
          params: { data:{id: item.id , name:item.name ,img:item.img,price:item.price}},
     }"
  >
   

    <v-img
      :src="item.img"
      max-height="120"
    ></v-img>

    <v-card-title>{{item.name}}</v-card-title>

    <v-card-text >
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