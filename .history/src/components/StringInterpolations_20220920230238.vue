<template>
    <div>
      <h5>HELLO {{user_name}}</h5>
    </div>
</template>

<script>
    export default {
      name: 'StringInterpolationsComponent',
      data: {
        user_name: 'NAUMAN'
      }  
    }
</script>

<style scoped>
    h5{
        color: orange;
    }
</style>