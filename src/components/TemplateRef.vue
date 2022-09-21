<template>
    <div>
        <input type="text" ref="inputRef"/>
    </div>
</template>

<script>
    export default {
        name: 'TemplateRefComponent',
        mounted(){
            this.$refs.inputRef.focus()
        }
    }
</script>

<style scoped>

</style>