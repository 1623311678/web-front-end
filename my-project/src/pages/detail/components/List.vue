<template>
  <div>

    <div
      class="item "
      v-for="(item, index) of list"
      :key="index"
    > <span class="iconfont icon-star item-icon"></span>
    
      <div class="item-title border-bottom">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-chilren " >
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array

  }
}
</script>

<style scoped>
.item-title{
      line-height:.8rem;
      height: .8rem;
      font-size:.5rem;
      padding:0 .2rem; 
      color:blue;
      display:inline-block; 

  }
  .item-icon{
    color:red;
    display:inline-block; 
      line-height:.6rem;
      font-size:.5rem;
     padding-top:.1rem;
  }
  .item-chilren{
    padding:0 .3rem;
 
  }
</style>
