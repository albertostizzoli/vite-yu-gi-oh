<template>
    <div class="container pt-3 pb-3">
        <div class="row">
            <div class="col-12">
                <select class="form-select" name="" id="" @change="sendValue" v-model="selected">
                    <option value="">Category</option>
                    <option v-for="(item, index) in onlyValue" :key="index" :value="item">{{ item }}</option>
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
            store,
            selected: ''
        }
    },
    computed: {
        onlyValue(){
            const only = [...new Set(store.cards_list.map((item) => item.type))];
            return only;
        }
    },
    methods: {
        sendValue() {
            this.$emit('search', this.selected)
        }
    }
}
</script>

<style lang="scss" scoped>
.form-select{
    width: 30%;
}

</style>