<template>
  <h2 v-for="(name,index) in names" :key="name">{{index}} {{name}}</h2>
</template>


<script>

export default {
  name: 'App',
  data(){
    return {
      names: ['Riley', 'Sara', 'Clia']
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
