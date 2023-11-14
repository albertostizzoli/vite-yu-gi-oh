<template>
    <div class="container pt-2">
        <div class="cards mb-2">
            <h4>Founded {{ numberResults }} cards</h4>
        </div>
        <div class="d-flex justify-content-between flex-wrap">
            <Card v-for="(item, index) in store.cards_list" :key="index" :card="item" />
        </div>
    </div>
</template>

<script>
import Card from './Card.vue';
import { store } from '../store.js';
export default {
    name: 'CardList',
    components: {
        Card
    },
    data() {
        return {
            store
        }
    },
    computed: {
        numberResults() {
            return store.cards_list.length
        }
    }
}
</script>

<style lang="scss" scoped>

.container {
    background-color: white;

    .cards{
        color: white;
        background-color: black;
        padding: 15px;
        margin-bottom: 10px;
    }
}
</style>