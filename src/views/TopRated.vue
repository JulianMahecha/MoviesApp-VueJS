<template>
  <div class="top-rated">
    <b-container>
      <b-row class="text-center">
        <b-col>1 of 3</b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from "axios";

export default {
  name: "top-rated",
  created: function() {
    let result = axios
      .get(
        "https://api.themoviedb.org/3/movie/top_rated?api_key=fccff7a20e96ef4b4191beea4a87a3e2&language=en-US&page=1"
      )
      .then(res => {
        console.log(res.data);
      })
      .catch(err => {
        console.log(err);
      });
  }
};
</script>
