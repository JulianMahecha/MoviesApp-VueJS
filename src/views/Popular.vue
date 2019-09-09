<template>
  <div class="top-rated p-2">
    <b-container class="mx-auto">
      <b-row class="text-center">
        <!-- Iteración -->
        <b-col md="3" v-for="movie of movies" v-bind:key="movie.id">
          <b-card
            :title="movie.title"
            :img-src='"https://image.tmdb.org/t/p/w1280/"+movie.poster_path'
            :img-alt='"https://image.tmdb.org/t/p/w1280/"+movie.poster_path'
            img-top
            tag="article"
            style="max-width: 20rem;"
            class="mb-2"
          >
          <!-- Texto de tarjeta -->
            <b-card-text>{{ movie.overview }}</b-card-text>
            <b-card-text>Calification: {{ movie.vote_average }}</b-card-text>

            <b-button :href='"https://www.themoviedb.org/movie/"+movie.id' variant="primary">See Details</b-button>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from "axios";

export default {
  name: "popular",
  data() {
    return {
      movies: []
    };
  },
  created() {
    this.fetch();
  },
  methods: {
    fetch() {
      let results = axios
        .get(
          "https://api.themoviedb.org/3/movie/popular?api_key=fccff7a20e96ef4b4191beea4a87a3e2&language=en-US&page=1"
        )
        .then(res => {
          this.movies = res.data.results;
        })
        .catch(err => {
          console.log(err);
        });
    }
  }
};
</script>
