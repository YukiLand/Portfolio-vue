<template>
<div id="app">
  <v-app>
    <v-app-bar
      color="white"
      dense
      white
    >

      <v-toolbar-title>Menu</v-toolbar-title>

      <v-spacer></v-spacer>

      <span>Qui suis-je</span>

      <v-spacer></v-spacer>

      <span>Professionnel</span>

      <v-spacer></v-spacer>

      <span>Contact</span>

        <button @click="myFunction()">Click Me</button>

      <v-spacer></v-spacer>

      <v-btn @click="github()" icon class="ma-2" outlined fab color="red">
        <v-icon>mdi-github</v-icon>
      </v-btn>



      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
            class="ma-2" outlined fab color="indigo"
          >
            <v-icon>mdi-flag</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    </v-app>
  </div>
</template>

<script>
  export default {
    el: '#app',
    name: 'navbar',

    data: () => ({

    }),
    methods: () => ({
      github: function() {
        window.open("https://github.com", "_blank"); 
      }
    })
  }
</script>
