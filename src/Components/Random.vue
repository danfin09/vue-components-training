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
        <p>Random value  {{ min }} and {{ max }} : {{ randomValue }}</p>
    </div>

</template>

<style>
div{
    color: royalblue;
    border: 1px solid rgb(62, 5, 5);
}
</style>