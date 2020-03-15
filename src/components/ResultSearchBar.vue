<template>
  <div class="result-search-bar">
    <img class="search-logo" src="./../assets/logo.png" @click="goHome" />
    <ResultSearchTpl :value="value" @change="$emit('input',$event)" />
  </div>
</template>
<script>
import ResultSearchTpl from "@/components/ResultSearchTpl.vue";

export default {
  name: "result-search-bar",
  props: ['value'],
  components: {
    ResultSearchTpl
  },
  methods:{
    goHome(){
      this.$router.push("/")
    }
  }
};
</script>
<style lang="less" scoped>
@import "./../themes/base.less";
.result-search-bar{
  text-align: left;
  padding: 2px;
  border-bottom: 1px solid #DFE1E5;
  margin-top: -14px;
}
.search-logo{
  height: @result-search-height;
  vertical-align: middle;
  margin-right: 20px;
}
.search-logo:hover{
  cursor: pointer;
}
</style>