<script setup>
import Card from './Card.vue'
import BoardList from './BoardList.vue'
import { ref } from 'vue';

let cards = 1
const componentsArray = ref([])

const addNewCard = () =>{
    
componentsArray.value.push(cards)

}
    


</script>




<template>

<BoardList class="boardSetup"></BoardList>



</template>
<style scoped>
  .boardSetup{
    position: fixed;
    top: 85px;
    left: 0px;

  }

</style>