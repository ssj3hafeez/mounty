<template>
  <div id="app">
     <Button/>
     <TweetCards />
     
     
  </div>
</template>

<script>
import TweetCards from './components/TweetCards.vue'
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Button,
    TweetCards
  
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
    color: #2c3e50;
  display: grid;
  gap: 10px;
  place-items: center;
}
</style>
