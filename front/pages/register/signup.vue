<template>
    <v-container class="">
      <v-row justify="center">
        <v-col cols="12" sm="8" md="6">
          <v-card class="elevation-12">
            <v-card-title class="headline grey lighten-2">
              <v-icon color="primary">mdi-account-plus</v-icon>
              Register!
            </v-card-title>
  
            <!-- <Notification :message="error" v-if="error"/> -->
  
            <v-form>
              <v-text-field
                v-model="username"
                label="Username"
                required
              ></v-text-field>
  
              <v-text-field
                v-model="email"
                label="Email"
                type="email"
                required
              ></v-text-field>
  
              <v-text-field
                v-model="password"
                label="Password"
                type="password"
                required
              ></v-text-field>
  
              <v-btn type="submit" color="black" block>
                Register
              </v-btn>
            </v-form>
  
            <div class="text-center mt-4">
              Already got an account?
              <nuxt-link to="/register/login" class="primary--text">Login</nuxt-link>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script setup>
//   import Notification from '@/components/Notification.vue';
  
  // Add your register function logic here
  
  </script>
  