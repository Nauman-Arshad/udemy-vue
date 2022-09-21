<template>
    <div class="card">
        <div id="card-h">
            <slot name="header"></slot>
        </div>
        <div id="card-c">
            <slot></slot>
        </div>
        <div id="card-f">
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CardComponent',
    }
</script>

<style scoped>
.card{
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.2s;
    padding: 16px;
    margin-bottom: 20px;
    width: 200px;
    font-weight: bold;
    word-spacing: 7px;
    letter-spacing: 4px;
}
.card:hover{
    color:orange;
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}
</style>