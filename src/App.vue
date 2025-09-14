
<script setup>
import { ref } from 'vue';

import IdCard from './Components/IdCard.vue';
import BoxColor from './Components/BoxColor.vue';
import Random from './Components/Random.vue';
import LikeButton from './Components/LikeButton.vue'; 



</script>


<template>
  
    <h1>Image Gallery</h1>
    <p>To create image of diverse Documents</p>

    <h2>Personal ID Cards</h2>

    <IdCard first-name="John" 
    last-name="Doe" 
    gender="male" 
    :height="189"
    picture="https://randomuser.me/api/portraits/men/44.jpg" 
    :birth="new Date('1990-07-01')" />

    <IdCard first-name="Maria" 
    last-name="Dolores" 
    gender="female" 
    :height="171"
    picture="https://randomuser.me/api/portraits/women/44.jpg" 
    :birth="new Date('1999-05-11')" />

    <h2>Box Colors</h2>
    <BoxColor :r="255" :g="0" :b="0" />
    <BoxColor :r="128" :g="255" :b="0" />


    <h2>Random Numbers</h2>
    <Random :min="1" :max="6" />
    <Random :min="1" :max="100" />



    <h2>Like Button</h2>
    <LikeButton />
    <LikeButton />
    



</template>


<style scoped>
h2 {
  margin: 1rem 0;
}

</style>
