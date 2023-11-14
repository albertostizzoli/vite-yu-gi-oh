<template>
    <div class="card text-center">
        <img :src="card.card_images[0].image_url" alt="card-image" @click="cardImageFullScreen">
        <span class="text-light name-card">{{ card.name }}</span>
        <span>{{ card.type }}</span>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        card: Object
    }

}
</script>

<style lang="scss" scoped>
.card {
    width: calc(100% / 5 - 20px);
    border: none;
    margin-bottom: 20px;
    background-color: #D48F38;

    .name-card {
        padding: 15px 0;
        text-transform: uppercase;
        font-size: 18px;
    }
}
</style>