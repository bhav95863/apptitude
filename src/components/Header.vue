<template>
  <v-app-bar app lgiht>
      <v-avatar tile height="48" width="auto">
        <img src="../assets/Logo_AptitudeTechnologies.png" alt="logo">
        <!-- <router-link height="40px" to="/"><img src="../assets/Logo_AptitudeTechnologies.png" alt="logo"></router-link> -->
      </v-avatar>
    
      <div class="flex-grow-1"></div>

      <v-toolbar-items>
        <v-btn text href="#/">Home</v-btn>
        <v-btn text href="#/about">About</v-btn>
        <v-btn text href="#/login">Login</v-btn>
        <v-menu left bottom offset-y close-on-click >
          <template v-slot:activator="{ on }">
            <v-btn text v-on="on">
              {{customer_email}}
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="n in menu_items"
              @click="() => {}"
              :key="n.id"
            >
              <v-list-item-title>{{ n.text }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-toolbar-items>
    </v-app-bar>

</template>

<script>
export default {
  name: "Header",
  data: () => ({
    customer_email : 'bhavesh@gmail.com',
    loggedIn : true,
    menu_items: [
      { id: 0, text: 'Vegetables' },
      { id: 1, text: 'Cheese' },
      { id: 2, text: 'Whatever' }
    ]
  })
};
</script>
