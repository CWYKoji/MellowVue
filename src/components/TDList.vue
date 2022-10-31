<script setup>
import { ref } from 'vue';
import TDListItem from './TDListItem.vue';
const listItems = ref([
    

])

const todo = ref('')

const addToList= () =>{

    listItems.value.push({
        task: todo.value,
        completed: false,
    })

    todo.value = ''
}

</script>

<template>

    
    <TDListItem v-for="item in listItems" :task="item.task" :completed="item.completed"></TDListItem>
    <input placeholder="add a todo" type="text" v-model="todo"  v-on:keyup.enter="addToList" />
    


    
        

    
</template>

<style scoped>
</style>