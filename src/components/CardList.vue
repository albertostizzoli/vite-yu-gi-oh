<template>
    <div v-if="store.loading" class="loading text-center">
        <h1>LOADING...</h1>
    </div>
    <div v-else class="container">
        <div class="cards">
            <h4>Founded {{ store.cards_list.length }} cards</h4>
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
    }
}
</script>

<style lang="scss" scoped>
.loading {
    height: calc(100vh - 80px);
    width: 100%;
}

.container {
    background-color: white;
    padding: 30px;

    .cards{
        color: white;
        background-color: black;
        padding: 15px;
        margin-bottom: 10px;
    }
}
</style>