<template>
      
    <v-app-bar
      app
      color="white"
      flat
    >
      <v-container class="py-0 fill-height">
        <v-avatar
          class="mr-10"
          color="grey darken-1"
          size="32"
        ></v-avatar>
        <h2>鴻升科技有限公司</h2>
        <v-btn
          v-for="link in links"
          :key="link"
          text
        >
          {{ link }}
        </v-btn>

        <v-spacer></v-spacer>
        
      
        <v-btn icon  to="/">
        <v-icon>mdi-home</v-icon>
      </v-btn>

      <v-btn icon to="/about">
        <v-icon>mdi-pharmacy</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-cart</v-icon>
      </v-btn>


      </v-container>
    </v-app-bar>
</template>