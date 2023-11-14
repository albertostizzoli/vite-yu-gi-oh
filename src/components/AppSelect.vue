<template>
    <div class="container">
        <div class="row m-3">
            <div class="col-12">
                <select name="" id="">
                    <option value=""></option>
                </select>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from '../store.js';
export default {
    name: 'AppSelect',
    data() {
        return {
            store
        }
    },
    methods: {
        sendValue() {
            this.$emit('search', store.selected)
        }
    }
}
</script>

<style lang="scss" scoped>

</style>