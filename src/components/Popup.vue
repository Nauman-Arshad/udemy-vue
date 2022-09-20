<template>
    <div>
<h2>This is the popup</h2>
<input type="text" v-model="name" />
<button @click="$emit('close')">Close popup</button>
    </div>
</template>

<script>
    export default {
        name: "PopupComponent",
        emits: {
            close: (name)=> {
                if(!name) {
                    return false
                } else {
                    return true
                }
            },
        },
        data(){
            return{
                name: ''
            }
        }
    }
</script>

<style scoped>

</style>