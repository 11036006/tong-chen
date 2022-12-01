<template>
  <div>
    <v-app-bar app color="#bbded6" flat>
      <v-container class="py-0 fill-height">
    
            <h2 >同晨科技有限公司</h2>
    
      
        

        <v-spacer></v-spacer>
        <div :class="$style.menu">
          <v-btn icon to="/">
            <v-icon>mdi-home</v-icon>
          </v-btn>

          <v-btn icon to="/about">
            <v-icon>mdi-information</v-icon>
          </v-btn>
          

          <v-btn icon>
            <v-icon>mdi-cart</v-icon>
          </v-btn>
        </div>
        <div :class="$style.drawer">
          <v-app-bar-nav-icon
            @click.stop="drawer = !drawer"
          ></v-app-bar-nav-icon>
        </div>
      </v-container>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute bottom temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item to="/">
            <v-btn icon>
              <v-icon>mdi-home</v-icon>
            </v-btn>
          </v-list-item>

          <v-list-item to="/about">
            <v-btn icon>
              <v-icon>mdi-information</v-icon>
            </v-btn>
          </v-list-item>

          

          <v-list-item>
            <v-btn icon>
              <v-icon>mdi-cart</v-icon>
            </v-btn>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
    };
  },
  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
<style module>
/* 在螢幕寬度 768px 以下，就會觸發menu 消失 */
@media (max-width: 768px) {
  .menu {
    display: none;
  }
}

/* 在螢幕寬度 768px 以上，就會觸發drawer 消失 */
@media (min-width: 768px) {
  .drawer {
    display: none;
  }
}
</style>