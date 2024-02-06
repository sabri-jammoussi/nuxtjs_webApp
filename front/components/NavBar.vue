<template>
    <v-card >
      <v-layout>
        <v-spacer></v-spacer>
        <!-- <v-system-bar color="deep-purple darken-3"></v-system-bar> -->
        <v-navigation-drawer v-model="drawer">
          <v-list :items="items"></v-list>
        </v-navigation-drawer>
        <v-app-bar color="primary" prominent>
          <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          <v-toolbar-title>My files</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-row class="d-flex justify-end mr-2">
      <v-menu
        min-width="200px"
        rounded
      >
        <template v-slot:activator="{ props }">
          <v-btn
          icon="mdi-dots-vertical "  
            v-bind="props"
      style="color: aliceblue;"
          >
          </v-btn>
        </template>
        <v-card>
          <v-card-text>
            <div class="mx-auto text-center">
              <v-avatar
                color="brown"
              >
                <span class="text">{{ userName }}</span>
              </v-avatar>
              <!-- <h3>{{userName}} {{ userLastName }}</h3>
              <p class="text-caption mt-1">
               {{userEmail}}
              </p>
              <v-divider class="my-3"></v-divider>
           <router-link to="/editprofile"> 
            <v-btn
                rounded
                variant="text"
              >
              Modifier le compte
              </v-btn>
           </router-link> -->
              <v-divider class="my-3"></v-divider>
          <nuxt-link  to="/register/login">
            <v-btn
                rounded
                variant="text"
              >
              Déconnecter
              </v-btn>
          </nuxt-link>
            </div>
          </v-card-text>
        </v-card>
      </v-menu>
    </v-row>
        </v-app-bar>
        <v-main style="height: 100vh;">
          <v-card-text>
            <!-- Your main content goes here (for example, the Home component) -->
            <Home />
         
          </v-card-text>
        </v-main>
        <v-footer color="rgb(220, 220,220)" app>
     

     <span style="color: #16DF17;">&copy; APBS</span>
   </v-footer>
      </v-layout>
      
  
    </v-card>
    
  </template>
  
  <script>
  import Home from "@/components/Home.vue";
  
  export default {
    components: {
      Home,
    },
    data: () => ({
      drawer: false,
      items: [
        { title: 'Foo', value: 'foo' },
        { title: 'Bar', value: 'bar' },
        { title: 'Fizz', value: 'fizz' },
        { title: 'Buzz', value: 'buzz' },
      ],
    }),
    watch: {
      group() {
        this.drawer = false;
      },
    },
  };
  </script>
  