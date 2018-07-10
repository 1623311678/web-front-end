<template>
    <div class="header"> 
<div class="header-left">
    <div class=" back-icon iconfont icon-set" ></div>
</div>
<div class="header-input">
    <span class="iconfont icon-sousuo" ></span>
    输入城市/景点/游玩主题</div>
    <router-link to='/city'>
<div class="header-right">{{this.city}}
    <span class="iconfont icon-moreunfold"></span>
</div>
    </router-link>
    </div>
</template>
<script>
import { mapState } from 'vuex'
export default {
    name:'HomeHeader',
    computed: {
        ...mapState(['city'])

    }
    
}
</script>
<style lang="" scoped>
.header{
    line-height: .86rem;
    display: flex;
    background: #00bcd4;
    color: #fff;
}
.header-left{
    width: .64rem;
    float:left;
}
.back-icon{
   text-align: center;
   font-size: .4rem;
   
}
.header-input{
    flex:1;
    background: #fff;
    border-radius:.1rem;
    margin-top:.12rem;
    height:.64rem;
    line-height:.64rem;
    margin-left:.2rem;
    color:#ccc;
  
}
.header-right{
    min-width: 1.04rem;
    padding:0 .1rem;
    float:right;
    text-align: center;
    color:white;
}

</style>


