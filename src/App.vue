<template>
 <v-app>
  
  <!-- container of v-app-bar -->
  <Header/>
      
  <!-- Sizes your content based upon application components -->
  <v-content>
    <!-- Provides the application the proper gutter -->
    <v-container fluid>
      <!-- If using vue-router -->
      <router-view></router-view>
      
    </v-container>
  </v-content>

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
</template>

<script>
import Header from './components/Header';



export default {
  name: 'App',
  components: {
    Header,
  },
  data: () => ({
    // 
  })
};
</script>