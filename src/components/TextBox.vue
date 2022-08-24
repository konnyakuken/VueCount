<template>
    <div>
        <input v-model="number" type="number" @keydown.enter="catchNum()">
    </div>
</template>
<script lang="ts" setup>
    import { ref } from 'vue';
    const emit = defineEmits(['change'])

    const number =ref(0) 
    function catchNum() {
        //number.value =10
        emit("change",number.value)
    }
    
</script>

<style scoped>

</style>
