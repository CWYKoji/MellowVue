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

    <div>
        <TDListItem v-for="item in listItems" :task="item.task" :completed="item.completed" ></TDListItem>
    </div>
    <div>
        <input placeholder="add a todo" type="text" v-model="todo" v-on:keydown.enter="addToList"/>
        <!-- <button>Add</button> -->
    </div>
</template>

<style scoped>
</style>