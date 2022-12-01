<template>
  <v-container style="overflow:scroll">
    <v-row>
      <v-col cols="2" :class="$style.list">
        <v-sheet rounded="lg">
          <v-list color="#bbded6">
            <v-list-item link v-on:click="gaTure">
              <v-list-item-content>
                <v-list-item-title> A4影印紙</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
           
             <v-list-item link v-on:click="frTure">
              <v-list-item-content>
                <v-list-item-title> A3影印紙 </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
           
            <v-list-item link v-on:click="seTure">
              <v-list-item-content>
                <v-list-item-title> B5影印紙 </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
         
           
               <v-divider class="my-2"></v-divider>
            <v-list-item link color="grey lighten-4"> </v-list-item>
          </v-list>
        </v-sheet>
      </v-col>

      <v-col cols="10" v-if="seafood">
        <v-sheet min-width="300">
          <Card :data="data[0].commodity" :class="$style.card" />
        </v-sheet>
      </v-col>
      <v-col cols="10" v-if="fruit">
        <v-sheet min-width="200">
          <Card :data="data[1].commodity" :class="$style.card" />
        </v-sheet>
      </v-col>
       <v-col cols="10" v-if="game">
        <v-sheet min-width="200">
          <Card :data="data[2].commodity" :class="$style.card" />
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import Card from "../components/Card.vue";
export default {
  components: {
    Card,
  },
  data() {
    return {
      fruit: false,
      seafood: false,
      game:true,
      data: [
        {
          class: "B5影印紙",
          commodity: [
            {
              id: 1,
              name: "Double A 多功能影印紙 B5 80G",
              img: "https://img.shopping.friday.tw/images/product/228/6849462/6849462_3_1.jpg?514947",
              price: "630",
            },
            {
              id: 2,
              name: "PaperOne 70G B5 多功能紙/影印紙",
              img: "https://s.yimg.com/zp/images/53B1D826C642192B371F10E13DE46C775D1FA367",
              price: "1090",
            },
          ] 
        },
        {
          class: "A3影印紙",
          commodity: [
            {
              id: 1,
              name: "Double A 多功能影印紙 A3 80G",
              img: "https://img.shopping.friday.tw/images/product/228/6849462/6849462_3_1.jpg?514947",
              price: "1200",
            },
            {
              id: 2,
              name: "BLC A3 多功能影印紙 70G",
              img: "https://i1.momoshop.com.tw/1619300799/goodsimg/0006/755/183/6755183_R_m.webp",
              price: "1120",
            },
            {
              id: 3,
              name: "PaperOne 70G A3 多功能紙/影印紙",
              img: "https://s.yimg.com/zp/images/53B1D826C642192B371F10E13DE46C775D1FA367",
              price: "1380",
            },
            {
              id: 4,
              name: "Quality A3 影印紙(包)",
              img: "https://online.carrefour.com.tw/on/demandware.static/-/Sites-carrefour-tw-m-inner/default/dw7b0a7113/images/large/0058713_quality-a3-.jpeg",
              price: "249",       
            },
            
          ],
        },
         {
          class: "A4影印紙",
          commodity: [
            {
              id: 1,
              name: "ARIA 事務用影印紙A4 70G ",
              img: "https://cs-c.ecimg.tw/items/DCAP02A900AVKJX/000001_1663924879.jpg",
              price: "520",
            },
            {
              id: 2,
              name: "Ecorox 高白環保影印紙 A4 70G",
              img: "https://cs-c.ecimg.tw/items/DCAP02A900F16CH/000001_1668996979.jpg",
              price: "500",
            },
            {
              id: 3,
              name: "Double A 多功能影印紙 A4 70G",
              img: "https://img.eclife.com.tw/photo2011/prod_2019/1/F5080275-A.jpg",
              price: "625",
            },
            {
              id: 4,
              name: "PaperOne copier 多功能影印紙 A4 70G ",
              img: "https://s.yimg.com/zp/MerchandiseImages/5CC3E1F483-SP-9788478.jpg",
              price: "1150",       
            },
            
          ],
        },
      ],
    };
  },
  mounted() {
    this.data;
  },
  methods: {
    frTure() {
      this.fruit = true;

      if (this.fruit) {
        this.seafood = false;
        this.game =false;
      }
    },
    seTure() {
      this.seafood = true;

      if (this.seafood) {
        this.fruit = false;
        this.game =false;
      }
    },
    gaTure(){
      this.game =true;
      if(this.game){
          this.seafood = false;
          this.fruit = false;
      }
    }
  },
};
</script>
<style module>

/* 在螢幕寬度 768px 以下，就會觸發menu 消失 */

@media (max-width: 768px) {
  .list {
    display: none;
  }
  .card {
    padding: 15px;
    font-size: 20px;
  }
}
</style>