<script setup>
    defineProps(['content'])
</script>
<template>
    <div class="div">
        <h1>{{ content }}</h1>
    </div>
</template>
<style>
    .div{
        margin: 0px;
        padding: 7.5px;
        background-color: dodgerblue;
        color: white;
        width: auto;
        height: fit-content;
    }
    h1{
        color: white;
    }
</style>