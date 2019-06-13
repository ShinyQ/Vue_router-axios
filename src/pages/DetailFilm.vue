<template>
   <div id="app">
        <div class="back"><router-link to="/"> Kembali Ke Home</router-link></div>
        <h1>Detail Film</h1>
        <GetDetailApi ></GetDetailApi>
  </div>
</template>

<script>
  import axios from 'axios'
  import GetDetailApi from '../components/GetDetailApi'
  export default {
    name: 'DetailFilm',
    components: {    
        GetDetailApi
    },
    data: function () {
        return {
            films:[] 
        }
    },
  }
</script>
<style>
    .back{
        text-decoration: none!important;
    }
</style>