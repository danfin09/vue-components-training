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
 width: 300px;
  height: 400px;
  border: 2px solid #333;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10px;
    font-size: 3rem;
    color: rgb(17, 1, 1);
;
}

</style>

