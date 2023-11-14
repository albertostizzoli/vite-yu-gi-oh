<template>
  <AppHeader />
  <main>
    <AppSelect @search="searchCard" />
    <CardList />
  </main>

</template>

<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppSelect from './components/AppSelect.vue';
import CardList from './components/CardList.vue';
import { store } from './store.js';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppSelect,
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
        setTimeout(()=>{
          store.loading = false;
        }, 2000)
      });
     },
    searchCard(type){
      let newUrl = store.url;
      if(type != '') {
        newUrl += `&type=${type}`;
        axios.get(newUrl).then((response) =>{
          store.cards_list = response.data.data;
        })
      } else{
        axios.get(store.url).then((response) =>{
           store.cards_list = response.data.data;
        })
      }
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