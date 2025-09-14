<script setup>

defineProps({
    firstName: String,
    lastName: String,
    gender: { type: String, 
        validator: value => ['male', 'female'].includes(value)},

    height: { type: Number, 
        validator: value => value > 0 }, 
    birth: { type: Date }, 
    picture: { type: String }
})
</script>

<template>

    <div class="card-container">
        <h1>ID Card</h1>
        <div class="id-card for male and female">
        </div>
        <img :src="picture" alt=" "/>

        <div>
            <p><strong>First name</strong> {{ firstName }}</p>
            <p><strong>Last name</strong> {{ lastName }}</p>
            <p><strong>Gender</strong> {{ gender }}</p>
            <p><strong>Height</strong> {{ height }}</p>
            <p><strong>Birth</strong> {{ birth }}</p>
        </div>
    </div>
</template>

<style scoped>
div.card-container {
    border: 4px solid #100101;
    padding: 2rem;
    border-radius: 8px;
    background-color: #f9f9f9;
}

img {
    width: 120px;
    height: auto;
    border-radius: 8px;
    margin-top: 1rem;
}


p {
    margin: 1rem 0;
    font-size: 1.5rem;
    color: #333;
    text-align: left;

}
</style>