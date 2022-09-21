<template>
 <Card>Card Content</Card>
 <Card><h2>I work on vue</h2></Card>
<Card>
  <img src="https://www.shutterstock.com/image-illustration/spectral-clouds-escape-reality-series-600w-1707615538.jpg"/>
</Card>
<Card>
  <template v-slot:header>
    <h3>Header</h3>
  </template>
  <template v-slot:default>
    <img src="https://www.shutterstock.com/image-illustration/spectral-clouds-escape-reality-series-600w-1707615538.jpg" />
  </template>
  <template v-slot:footer>
    <button>View Details</button>
  </template>
</Card>
<NameList>
  <template v-slot:default = 'slotProps'>
   {{slotProps.fname}} {{slotProps.lname}}
  </template>
</NameList>
<NameList>
  <template v-slot:default='slotProps'>
    {{slotProps.lname}} {{slotProps.fname}}
  </template>
</NameList>
</template>

<script>

import Card from './components/Card.vue';
import NameList from './components/NameList.vue';
export default {
  name: 'App',
  components: {
    Card,
    NameList
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
img{
  width:100%
}
</style>
