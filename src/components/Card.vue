<template>
<div class="d-flex justify-start mb-6">
  
  <v-card
    :loading="loading"
    max-width="30%"
    v-for="item in data" :key="item"
    :to="{
          name: 'Product',
          params: { data:{id: item.id , name:item.name ,img:item.img,price:item.price}},
        }"
  >
   

    <v-img

      max-width="100%"
      :src="item.img"
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