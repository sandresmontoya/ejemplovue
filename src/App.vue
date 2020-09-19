<template>
<v-content>
  <Toolbar/>
    <v-main>
     <Search v-on:searchResult="searchResult"/>
     <ImageList v-bind:items="items"/>
    </v-main>
</v-content>  
</template>

<script>

import Toolbar from './components/Toolbar'
import Search from './components/Search'
import ImageList from './components/ImageList'


export default {
  name: 'App',

  components: {
    Toolbar,
    Search,
    ImageList,
  },

  methods:{
    searchResult(response){
      this.items=response;
      console.log(this.items);

    }
  },

  data: () => ({
    items:[],
  }),
};
</script>
