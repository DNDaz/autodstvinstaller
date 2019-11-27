<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          :src="require('./assets/logo.png')"
          transition="moveInandOut"
          width="400"
        />

        <!--v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        /-->
      </div>
       <div>
          <v-btn color="#a4f9ef7F" mode="out-in" appear> Get a Quote </v-btn> 
          <br/>or Call Us on <v-icon>mdi-phone</v-icon> <b>073 853 7803</b>
        </div>
      <v-spacer></v-spacer>

      <v-btn
        text
        v-for="menuItem in menuItems"
        :key="menuItem.title"
        :to="menuItem.link"
      >
        <span class="mr-2">{{menuItem.title}}</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
          <router-view/>
    </v-content>
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',

  // components: {
  //   HelloWorld
  // },

  data: () => ({
    menuItems: [
      { title: 'home', link: '/', icon: 'mdi-home' },
      { title: 'about us', link: '/about', icon: 'mdi-anchor' },
      { title: 'product & services', link: '/products', icon: 'mdi-watch' },
      { title: 'contact', link: '/contacts', icon: 'mdi-tilde' }
    ]
    //

  })
}
</script>
<style>
.moveInandOut-enter-active .moveInandOut-leave-to-active {
  transition: all 1s;
}
.getAQuoteAPPBar{
  background-color: #000000;
}  
.fade-enter{
        opacity: 0;
    }
  .fade-enter-active{
      transition: opacity 1s;
  }
  .fade-leave{
      /* opacity: 1; */
  }
  .fade-leave-active{
      transition: opacity 1s;
      opacity: 0;
  }
 


</style>
