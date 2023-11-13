<template>
    <div class="container d-flex flex-wrap">
        <Card v-for="(item, index) in store.cards_list" :key="index" :card="item" />
    </div>
</template>

<script>
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

<style lang="scss" scoped></style>