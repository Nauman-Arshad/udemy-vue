<template>
    <div v-for="name in names" :key="name.fname">
     <slot :fname="name.fname" :lname= "name.lname"></slot>
     </div>
</template>

<script>
    export default {
     name: 'NameListComponent',
     data(){
        return {
           names: [
             {
                fname: 'NAUMAN',
                lname: 'KHAN',
             },
             {
                fname: 'JORGE',
                lname: 'FINCH',
             },
             {
                fname: 'MIC',
                lname: 'IN',
             },
          ]
        }
     }  
    }
</script>

<style scoped>

</style>