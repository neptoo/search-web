<template>
  <div class="result-search-tpl">
    <input
      class="input-search"
      :value="value"
      @keydown.enter="doSearch"
      @input="doInputChange"
    />
    <button class="btn-search" @click="doSearch">
      <img class="icon-search" src="./../assets/search.svg" />
    </button>
  </div>
</template>
<script>
export default {
  name: "result-search-tpl",
  props: {
    value: String
  },
  methods: {
    doInputChange(event) {
      this.$emit("change", event.target.value);
    },
    doSearch() {
      if (this.search !== "") this.$router.push(`/search/${this.search}`);
    }
  }
};
</script>
<style lang="less" scoped>
@import "./../themes/base.less";
.result-search-tpl {
  width: 400px;
  position: relative;
  display: inline-block;
}
.input-search {
  width: 100%;
  height: @result-search-height;
  border-radius: @result-border-radius;
  border: 1px solid #dfe1e5;
  padding: 20px;
  box-sizing: border-box;
  font-size: 1rem;
}
.btn-search {
  height: @result-search-height;
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}
.icon-search {
  width: 20px;
  height: 20px;
  margin-right: 15px;
}
</style>
