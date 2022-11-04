<script setup>
import { ref } from 'vue';
import TDListItem from './TDListItem.vue';

const listItems = ref([
    

])

const todo = ref('')

const addToList= () =>{

    listItems.value.push({
        task: todo.value,
        
    })

    todo.value = ''
}

</script>

<template>

    <div>
        <TDListItem v-for="item in listItems" :task="item.task"></TDListItem>
    </div>
    <div class="taskContainer">
        <input class="newTaskTitle" placeholder="Add a Task" type="text" v-model="todo" v-on:keydown.enter="addToList"/>
    </div>
    <div class="taskContainer">  
        <button class="butAddList" type="button" @click="addToList"> Add</button>
    </div>
   
    
    
</template>

<style scoped>



.newTaskTitle{
    width: 100%;

}
.butAddList{
  display: flex;   
  align-self: center;
}



</style>