<template>
  <div class="home">
    <h4>Film Bagus</h4>
    <div class="row">
      <div class="col s4" v-for="item in film" :key="item.id">
        <!-- card -->
        <div class="card">
          <div class="card-image waves-effect waves-block waves-light">
            <img class="activator" :src="item.Poster">
          </div>
          <div class="card-content">
            <span class="card-title activator grey-text text-darken-4">{{item.Title}}<i class="material-icons right">more_vert</i></span>
            <p><a href="" target="_blank">Selengkapnya</a></p>
          </div>
          <div class="card-reveal">
            <span class="card-title grey-text text-darken-4">{{ item.Year }}<i class="material-icons right">close</i></span>
            <p>{{ item.Title }}</p>
            <p>{{ item.imdbID }}</p>
          </div>
        </div>
        <!-- card -->
      </div>
    </div>
  </div>
</template>

<script>
  //import axios
  import axios from "axios";

  export default {
    name: 'HomeView',
    //membuat properti 
    data: function() {
      return {
        film: {}
      }
    },
    created() {
      this.getData();
    },
    methods: {
      getData() {
        axios
        .get('https://omdbapi.com/?s=Godzilla&apikey=7e263308')
        .then(response => {
          console.log(response.data.Search);
          //memasukkan data ke properti articles
          this.film=response.data.Search;
        })
      }
    }
  }
</script>

<style scoped>

</style>
