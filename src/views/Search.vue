<template>
  <div class="search">
    <ResultSearchBar v-model="search" />
    <div v-for="info in searchResultList" :key="info.id">
      <ResultSearchItem :info="info" />
    </div>
  </div>
</template>
<script>
import ResultSearchBar from "@/components/ResultSearchBar.vue";
import ResultSearchItem from "@/components/ResultSearchItem.vue";
import ResultSearchTpl from "@/components/ResultSearchTpl.vue";

const DB = require("./../data/search.json");

export default {
  name: "Search",
  components: {
    ResultSearchBar,
    ResultSearchItem,
    ResultSearchTpl
  },
  data() {
    return {
      search: this.$route.params.searchText,
      searchResultList: []
    };
  },
  created(){
    this.doSearchResult()
  },
  beforeRouteUpdate(to, from, next){
    next()
    this.doSearchResult();
  },
  methods: {
    doSearchResult() {
      const { searchText } = this.$route.params;
      if (DB.hasOwnProperty(searchText)) {
        this.searchResultList = DB[searchText];
      } else {
        this.searchResultList = [];
      }
    }
  }
};
</script>
