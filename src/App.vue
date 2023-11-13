<template>
  <AppHeader />
  <main>
    <CardList />
  </main>

</template>

<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';
import { store } from './store.js';

export default {
  name: 'App',
  components: {
    AppHeader,
    CardList,
  },
  data() {
    return {
      store
    }
  },
  methods: {
     getCards(){
      axios.get(store.url).then((response) =>{
        store.cards_list = response.data.data;
        console.log(store.cards_list);
      })
     }
  },
  created(){
    this.getCards();
  },
}
</script>

<style lang="scss">
@use './assets/styles/main.scss' as *;
</style>