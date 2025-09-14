<script setup>
const props = defineProps({
    r: Number,
    g: Number,
    b: Number
});

const color = `rgb(${props.r}, ${props.g}, ${props.b})`;
</script>

<template>
    
    <div class="boxes container " :style="{ backgroundColor: color }">
       RGB({{ props.r }}, {{ props.g }}, {{ props.b }})
    </div>

</template>

<style scoped>

.box {
 width: 200px;
  height: 100px;
  border: 2px solid #333;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10px;
    font-size: 1.8rem;
}

</style>

