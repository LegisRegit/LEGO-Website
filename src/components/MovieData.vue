<template>
  <div class="movieData" id="json">
    <div class="form-inline p-5">
      Movie Title:
      <br>
      <div class="form-group">
        <input class="form-control" type="text" v-model="title">
        <button class="btn btn-primary" @click="search">Search</button>
      </div>
    </div>

    <div v-if="movie != undefined" class="p-4">
      <img :src="movie.Poster">
      <h1>
        {{movie.Title}}
        <small>{{movie.Year}}</small>
      </h1>
      <h4>{{movie.Plot}}</h4>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      title: "Avatar",
      movie: undefined
    };
  },
  methods: {
    search() {
      fetch("http://www.omdbapi.com/?apikey=4fe797d4&t=" + this.title).then(
        res => {
          res.json().then(data => {
            this.movie = data;
          });
        }
      );
    }
  }
};
</script>


<style>
.movieData {
  padding-top: 4rem;
  min-height: 400px;
}
</style>
