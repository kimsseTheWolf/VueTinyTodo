<script setup>
    import {ref} from 'vue'
    const props = defineProps(['content', 'color'])
    const events = defineEmits(['buttonClicked'])
    const color = ref(props.color)

    function onButtonClicked(){
        events('buttonClicked')
    }
</script>
<template>
    <div :class="color" id="btn">
        <a @click="onButtonClicked()">{{ content }}</a>
    </div>
</template>
<style>
    #btn{
        margin: 5px;
        padding: 5px;
        border-radius: 5px;
        cursor: pointer;
        color: white;
        text-decoration: none;
        font-weight: bolder;
        font-size: large;
        text-align: center;
        width: fit-content;
        height: auto;
        display: inline-block;
    }
    .red{
        background-color: red;
    }
    .red:hover{
        background-color: rgb(161, 0, 0);
    }
    .blue{
        background-color: dodgerblue;
    }
    .blue:hover{
        background-color: rgb(16, 81, 146);
    }
    .green{
        background-color: rgb(20, 168, 72);
    }
    .green:hover{
        background-color: rgb(12, 105, 44);
    }
</style>