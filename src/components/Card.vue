<template>
    <div class="card text-center">
        <img :src="card.card_images[0].image_url" alt="Card">
        <span class="text-dark name-card">{{ card.name }}</span>
        <span>{{ card.archetype }}</span>
    </div>
 
</template>

<script>
    export default {
        props: {
            card: Object
        }
        
    }
</script>

<style lang="scss">
.card {
    width: calc(100% / 5 - 20px);
    background-color: #D48F38;
    border: none;
    margin-bottom: 15px;

    .name-card {
        padding: 15px 0;
        text-transform: uppercase;
        font-size: 18px;
    }
}


</style>