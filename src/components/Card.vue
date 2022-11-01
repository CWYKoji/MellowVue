<script setup>
  import { ref } from 'vue';
  import TDList from './TDList.vue'

  const title = ref('')
</script>

<template>
  <form>
    <div class="card">
      <div class="cardTitle">
        <input class="inputCardTitle" type="text" name="title" v-on:keydown.enter.prevent/>
      </div>
        <div class ="cardContents">
          <TDList></TDList>
        </div>
    </div>
  </form>
</template>

<style scoped>

.card{
    height: auto;
    width: 175px;
    border-color: black;
    border-width: 1px;
    border-style: double;
    flex-direction: column;
    position: fixed;
    top: 85px;
    left: 10px;
    overflow-x: hidden;
    overflow-y: auto;
}

.cardContents{
  width: 100%;
}

.inputCardTitle{
  width: 100%;
  height: 25px;
  border-style:hidden; 
}

.inputCardContents{
  width: 100%;
  height: 120px;
  border-style: hidden;
  
}

</style>