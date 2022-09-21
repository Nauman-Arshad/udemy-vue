<template>
    <div>
        <button @mouseover="incrementCount">Clicked {{count}} times</button>
    </div>
</template>

<script>
    import CounterMixin from '../mixins/counter'
export default {
    name: 'HoverCounterComponent',
    mixins: [CounterMixin],
}
</script>

<style scoped>

</style>