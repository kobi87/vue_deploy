<template>
  <v-app id="app" 
   >
    <v-app-bar app color="teal lighten-2" dark>
      <v-toolbar-title>AI Dashboard</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text rounded>Home</v-btn>
      <v-btn text rounded>Login</v-btn>
    </v-app-bar>
    <v-content>
      <HelloWorld/>
    </v-content>
  <v-footer color="teal lighten-3" padless>
    <v-row justify="center" no-gutters >
      <v-btn v-for="link in links" :key="link" color="white" text rounded class="my-2">
        {{ link }}
      </v-btn>
      <v-col class="teal lighten-2 py-4 text-center white--text" cols="12">
        {{ new Date().getFullYear() }} — <strong>© by Bewave</strong>
      </v-col>
    </v-row>
    </v-footer>  
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us',
      ],
  }),
};
</script>

<style>
   #app {
     background-image: url('https://www.technocrazed.com/wp-content/uploads/2015/12/Home-Wallpaper-9.jpg');
     /* background-color: #8f2c2c; */
    height: 100%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
  }
</style>
