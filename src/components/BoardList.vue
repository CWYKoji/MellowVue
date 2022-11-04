<script setup>
import { ref } from 'vue';
import BoardListItem from './BoardListItem.vue'
import IconNewFile from './icons/IconNewFile.vue'

const listItems = ref([
    

])

const todo = ref('')

const addToList= () =>{

    listItems.value.push({
        task: 1,
        
    })

    todo.value = ''
    
}

</script>

<template>
    <div class = "cardsComponents">
        <div class = "cardsArray">
            <BoardListItem v-for="item in listItems"></BoardListItem>
        </div>
        <div class="taskContainer">  
            <button class="butAddList" type="button" @click="addToList" > 
                Add Card
                <IconNewFile/>
            </button>
        </div>
    </div>
   
    
    
</template>

<style scoped>



.newTaskTitle{
    width: 100%;

}
.butAddList{
  display: flex;   
  align-self: center;
  margin-left: 10px;
}

.cardsArray{
    display: flex;
}
.cardsComponents{
    display: flex;
}



</style>