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

    <div class="card-container" style=" border: 1px solid black;">
       
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
    box-sizing: border-box;
    display: flex;
    border: 2px solid #100101;
    padding: 1rem;
    border-radius: 2px;
    background-color: #f9f9f9;
    margin: 1rem;

}

img {
    width: 120px;
    height: 120px;
    border-radius: 4px;
    margin-top: 1rem;
    align-items: left;
    margin-right: 2rem;
    
}


p {
    margin: 1rem 0;
    font-size: 1.5rem;
    color: #060404;
    text-align: left;
    flex: 1;

}

</style>