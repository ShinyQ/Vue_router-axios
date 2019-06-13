<template>
    <tbody>
        Episode ID : {{ films.episode_id }}<br><br>
        Judul Film : {{ films.title }}<br><br>
        Director : {{ films.director }} <br><br>
        Deskripsi : <br><br>{{ films.opening_crawl }}<br><br>
        Release Date : {{ films.release_date }} <br><br>
    </tbody>
</template>

<script>
  import axios from 'axios'
  export default {
    name: 'GetDetailApi',
    props: {
            film: String,
    },
    data: function () {
        return {
            films:[] 
        }
    },
    methods: {
      fetchDetailFilms: function () {
        axios.get('https://swapi.co/api/films/' + this.$route.params.id).then((response) => {
          this.films = response.data
          console.log(response.data)
        }, (error) => {
          console.log(error)
        })
      }
    },
    mounted: function () {
      this.fetchDetailFilms()
    }
  }
</script>>