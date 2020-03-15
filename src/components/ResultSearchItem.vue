<template>
  <div class="search-result-item">
    <a class="title link" :href="info.url">{{info.title}}</a>
    <div class="des">{{info.date}} - {{info.des}}</div>
    <div class="url">{{info.url}}</div>
  </div>
</template>
<script>
export default {
  name:'result-search-item',
  props:['info']
}
</script>
<style lang="less" scoped> 
.search-result-item{
  // border: 1px solid #333;
  text-align: left;
  padding: 20px;
  max-width: 660px;
}
.title{
  color: #001BA0;
  // font-size: 20px;
  font-size: 1.2em;
}
.link{
  text-decoration: none;
}
a:hover{
  text-decoration: underline;
}
.des{
  color: #666666;
  font-size: 13px;
  font: 13px/normal Arial,Helvetica,Sans-Serif;
  margin: 4px;
}
.url{
  color: #006D21;
  font-size: 14px;
  font-family: Arial, Helvetica, sans-serif;
}
</style>