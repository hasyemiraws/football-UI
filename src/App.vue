<template>
  <div>
    <Header/>
    <div class="container mx-auto px-3 mt-10">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import './scss/index.scss';

export default {
  components: {
    Header,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;700&display=swap');

#app {
  font-family: 'Poppins', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  background-color: #FBFBFB;
}
</style>
