<script setup>
import { ref } from 'vue'
const randomValue = ref(0);

const props = defineProps({
    min: Number,
    max: Number
})
const getRandomValue = (min,max) => {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

</script>

<template>
    <div>
        <div class="boxes container ">
            
        </div>
        
        <p>Random value  {{ min }} and {{ max }} : {{ randomValue }}</p>
        <span class="arrow">=></span>
        <span class="value">{{ randomValue }}</span>
        <button @click="randomValue = getRandomValue(props.min, props.max)">Generate</button>
        
        
         
    </div>

</template>

<style scoped>
div{
    color: rgb(0, 3, 10);
    border: 1px solid rgb(62, 5, 5);
    font-size: 2rem;
    background-color: aliceblue;

}
</style>