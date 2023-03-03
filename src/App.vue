<script setup>
    import checkList from './components/checkList.vue'
    import headerBox from './components/headerBox.vue'
    import prettyButtun from './components/button.vue'
    import inputArea from './components/inputArea.vue'
    import { ref } from 'vue';

    // const headerContent = ref(this.$refs.headerBox.content)
    const targetAddingTodoName = ref("")
    const todoList = ref([])

    function createNewTodo(todo_name){
        let targetTodo = {"title": todo_name, "isFinished": false};
        todoList.value.push(targetTodo)
    }
    
</script>
<template>
    <headerBox content="Tiny Todo" ref="headerContent"/>
    <div v-for="item in todoList">
        <checkList :title="item.title" content="" :isChecked="item.isFinished"/>
    </div>
    
    <div class="input-box">
        <inputArea v-model="targetAddingTodoName"/>
        <prettyButtun content="Add" color="blue" @buttonClicked="createNewTodo(targetAddingTodoName)"/>
    </div>
    
    <p>
        {{ targetAddingTodoName }}
    </p>
</template>
<style>
body{
    margin: 0px;
    background-color: #1f1f1f;
    font-family: Arial, Helvetica, sans-serif;
}
.input-box{
    background-color: #4a4949;
    margin: 5px;
    padding: 5px;
    border-radius: 5px;
    width: auto;
    height: fit-content;
}
</style>