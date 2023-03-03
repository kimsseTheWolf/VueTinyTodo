<script setup>
import { ref } from 'vue';

    defineProps(['title', 'content', 'isChecked'])
    const isChecked = ref(false)
</script>
<template>
    <div class="list-item">
        <input type="checkbox" v-model="isChecked" class="checkbox">
        <span class="span">
            <h2>{{ title }}</h2>
            {{ content }}
        </span>
    </div>
</template>
<style>
    .checkbox{
        width: 25px;
        height: 25px;
        border-radius: 5px;
        margin: 5px;
        display: inline-block;
        vertical-align: middle;
    }
    .list-item{
        margin: 7px;
        padding: 5px;
        border-radius: 5px;
        background-color: #323232;
        color: white;
        width: auto;
        height: fit-content;
    }
    .list-item:hover{
        background-color: #4a4949;
    }
    .span{
        width: 50%;
        height: fit-content;
        padding: 5px;
        display: inline-block;
        vertical-align: middle;
    }
    h2{
        color: white;
    }
</style>