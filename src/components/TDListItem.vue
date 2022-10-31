
<script setup>
const props = defineProps({
    task:{
        type: String,
    },
    completed: {
        type: Boolean
    }

})

</script>
<template>
    <div class ="listItem">{{props.task}}</div>
    
</template>

<style scoped>
.completed{
    text-decoration: line-through;
}

</style>