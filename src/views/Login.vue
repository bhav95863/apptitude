<template>
  <v-card width="400" class="mx-auto mt-10">
    <v-card-title>Login</v-card-title>
    <v-card-text>
      <v-form @submit="checkLogin">
        <v-text-field label="Username" v-model="username" prepend-inner-icon="mdi-account-circle"/>
        <v-text-field label="Passowrd" v-model="password" type="password" prepend-inner-icon="mdi-lock"/>
        <v-card-actions>
          <v-btn type="submit">Login</v-btn>  
        </v-card-actions> 
      </v-form>
    </v-card-text>
    
  </v-card>
</template>


<script>
import axios from 'axios';

export default {
  name: 'Login',
  data: () => ({
    username : '',
    password : ''
  }),
  methods :{
    checkLogin(e) {
      e.preventDefault();
      // console.log(this.username+' '+this.password);
      // axios.post("http://jsonplaceholder.typicode.com/posts", {
      // axios.post("http://35.231.57.152/api/method/login", {
      //             'accept': 'application/json',
      //             'accept-language': 'en_US',
      //             'Access-Control-Allow-Origin':'*',
      // 'Access-Control-Allow-Credentials':'true',
      // 'Access-Control-Allow-Methods':'GET, POST, OPTIONS',
      // 'Access-Control-Allow-Headers':'Authorization,DNT,X-Mx-ReqToken,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type',
      // 'Access-Control-Max-Age':1728000,
      // 'Content-Length':0,
      axios.post("http://demo.yopentech.com/api/method/login", {
        // headers: {
        //   'accept': 'application/json'
        // }, 
        data: {
          usr: this.username, 
          pwd: this.password
        }
      })
      .then(response => {response})
      .catch(e => {
        console.log(e);
      })

      
    }
  }
}
</script>