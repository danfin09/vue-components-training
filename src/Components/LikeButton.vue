<script setup>
import { ref } from 'vue';
const likes = ref(0);
const props = defineProps({
    colors: {
        type: Array,
        default: ( ) => ['purple','blue','green','yellow','orange','red']
    }
});

const currentColor = ref(props.colors[0]);
const handleLike = () => {
    const currentIndex = props.colors.indexOf(currentColor.value);
    const nextIndex = (currentIndex + 1) % props.colors.length;
    currentColor.value = props.colors[nextIndex];
    likes.value += 1;
};

</script>

<template>
  < <button 
    class="like-button" 
    @click="handleLike"
    :style="{ backgroundColor: currentColor }"
    
  >
    {{ likes }} {{ likes === 1 ? 'Like' : 'Likes' }} 
    
  </button>


</template>

<style scoped>
.boxes-container {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin-top: 40px;
}
.like-button {
  border: none;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  cursor: pointer;
}
.like-button:hover {
  transform: scale(1.05);
}

</style>