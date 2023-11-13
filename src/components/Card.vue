<template>
    <div>
        <img :src="card.card_images[0].image_url_small" alt="Card">
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

</style>