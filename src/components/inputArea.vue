<script setup>
    import prettyButton from './button.vue'
    defineProps(['modelValue'])
    defineEmits(['update:modelValue'])
</script>
<template>
    <input placeholder="Enter the task you want to do here!" 
        :value="modelValue" 
        @input="$emit('update:modelValue', $event.target.value)"
        class="target-input">
</template>
<style>
    .target-input{
        width: 1000px;
        height: 25px;
        background-color: #4a4949;
        border-color: white;
        border-radius: 5px;
        color: white;
    }
</style>