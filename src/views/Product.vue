<template>
<v-row  class="pa-4">
 <br>
<v-col >
<v-img
   max-width="600px"
   max-height="550px"
  :src="newDate.img"
></v-img>
</v-col>
<v-col>
<h1>{{newDate.name}} </h1> 
<h1>${{newDate.price}}</h1>

 <v-btn block>
    加入購物車
  </v-btn>
</v-col>
</v-row>  
</template>
<script>
export default {
    props:{
        data:Array
    },
    data(){
      return{
          newDate:this.data
      }
    },
}
 
</script>