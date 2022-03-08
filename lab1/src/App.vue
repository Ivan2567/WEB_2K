<template>
    <div id='app'>
        <h2>{{ myname}}</h2>
        <vtsu :page = "page"></vtsu>
        <regform></regform>
    </div>
    
</template>

<script lang="ts">
//import Vue from 'vue';
import vtsu  from '../../vt-su/src/components/vtsu.vue'
import regform from '../../regform/src/components/regf.vue'
declare var require: any;
import { defineComponent } from 'vue';
import axios from 'axios';
var url = 'https://yandex.ru/';
export default defineComponent({
name: 'App',
components: {vtsu, regform},
data(){
  return{
      myname: require('get-my-myname'),page:[]
      };
    },
    mounted(){
      axios
      .get(url,
      { headers: {"Access-Control-Allow-Origin" : "https://yandex.ru/" },
      withCredentials: false,}
    ).then((response: any) =>
        {this.page = response.data;},
        ); 
  }, 
  });
</script> 
