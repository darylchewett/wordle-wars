<template>
  <div class="home">
    <h1 style="margin-bottom: 50px">Wordle Wars</h1>
    <button v-on:click="$router.push('Wordle')">Puzzlemaster mode</button>
    <br />
    <button v-on:click="notForYou">"Classic" mode</button>
    <br />
    <button v-on:click="$router.push('About')">About</button>
  </div>
</template>

<script>
import router from '@/router'
export default {
  name: 'Home',
  setup() {
    function notForYou() {
      alert('Coming Soon! (tm)')
    }

    return { notForYou }
  },
}
</script>

<style scoped>
button {
  font-size: xx-large;
  margin-bottom: 25px;
  background-color: #dd9296;
  border-radius: 10px;
  padding: 5px;
  width: 20ch;
}

button:hover {
  background-color: #f2b7c6;
}
</style>
