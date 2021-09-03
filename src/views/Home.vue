<template>
   <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet rounded="lg">
              <v-list color="transparent">
                <v-list-item
                  v-for="item in data"
                  :key="item"
                  link
                >
                  <v-list-item-content>
                    <v-list-item-title>
                      {{ item.class}}
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider class="my-2"></v-divider>

                <v-list-item
                  link
                  color="grey lighten-4"
                >
                 
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>

          <v-col cols="10">
            <v-sheet
              min-height="70vh"
            
              rounded="lg"
            >
              <Card :data="data[0].commodity" />
           
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
</template>
<script>
import Card from '../components/Card.vue'
export default {
  components:{
    Card
  },
  data(){
  
    return{
       data:[{
       class:"所有商品",
       commodity:[
         {
          id:1,name:"大明蝦",img:"https://starlight659.webnode.tw/_files/200000008-6259862599/450/d354e94702ebe346066c770784cd7703-max-w-1024.jpg?ph=751cc27414",price:"2000"
         },
         {
          id:2,name:"冷凍母香魚",img:"https://starlight659.webnode.tw/_files/200000001-9930499306/450/dafd3f0eb3d35f8fd6ae6301b8ebddea-cr-260x260.jpg?ph=751cc27414",price:"455"
         },
         {
         id:3,name:"冷凍公香魚",img:"https://starlight659.webnode.tw/_files/200000003-84cf784cf9/450/2647f34ffec1cff9faca76638d92fcc6-max-w-1024.jpg?ph=751cc27414",price:"250" 
         },
         
       ]},{class:"蝦"},{class:"貝"},{class:"全魚"}]

    }
  }
  
}
</script>