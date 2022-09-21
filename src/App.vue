<template>
  <teleport to="#portal">
   <Portal/>
  </teleport>
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
<h4>App Component Text </h4>
<ChildStyles/>
<button @click="activeTab = 'TabA'">Tab A</button>
<button @click="activeTab = 'TabB'">Tab B</button>
<button @click="activeTab = 'TabC'">Tab C</button>
<button @click="activeTab = 'TabD'">Tab D</button>
<!-- <TabA v-if="activeTab === 'TabA'"/>
<TabB v-if="activeTab === 'TabB'"/>
<TabC v-if="activeTab === 'TabC'"/> -->
<keep-alive>
<component :is="activeTab"/>
</keep-alive>
</template>

<script>

import Card from './components/Card.vue';
import NameList from './components/NameList.vue';
import ChildStyles from './components/ChildStyles.vue';
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';
import TabD from './components/TabD.vue';
import Portal from './components/Portal.vue';
export default {
  name: 'App',
  components: {
    Card,
    NameList,
    ChildStyles,
    TabA,
    TabB,
    TabC,
    TabD,
    Portal
},
data(){
  return{
    activeTab: 'TabA'
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
img{
  width:100%
}
h4{
  color: red
}
</style>
