<template>
    <div>
<h2>This is the popup</h2>
<button @click="$emit('close')">Close popup</button>
    </div>
</template>

<script>
    export default {
        name: "PopupComponent",
        emits: ["close"]
    }
</script>

<style scoped>

</style>