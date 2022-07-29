<template>
  <h2 v-for="(name,index) in names" :key="name">{{index}} {{name}}</h2>
  <h2 v-for="name in fullNames" :key="name.first">{{name.first}} {{name.last}}</h2>

  <div v-for="actor in actors" :key="actor.name">
    <h2>{{actor.name}}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
  </div>
</template>


<script>

export default {
  name: 'App',
  data(){
    return {
      names: ['Riley', 'Sara', 'Clia'],
      fullNames:[
        {first: 'Riley', last: 'Van'},
        {first: 'Sara', last: 'Lana'},
        {first: 'Clia', last: 'Lin'},
      ],
      actors:[
        {
          name: 'Christian Bale',
          movies: ['Batman', 'The Prestige'],
        },
        {
          name: 'Di Caprio',
          movies: ['Titanic', 'Inception']
        }
      ]
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline{
  text-decoration: underline;
}
</style>
