<template>
  <StringInterpolations/>
  <button @click="showPopup = true">Show popup</button>
  <Popup v-show="showPopup" @close="showPopup = false" />
</template>

<script>
import StringInterpolations from './components/StringInterpolations.vue';
import Popup from './components/Popup.vue';
export default {
  name: 'App',
  components: {
    StringInterpolations,
    Popup
},
data() {
return{
  showPopup: false,
}
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
  margin-top: 60px;
}
</style>
