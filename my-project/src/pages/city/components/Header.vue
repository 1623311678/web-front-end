<template>
    <div class="header">
        城市选择
        <router-link to='/'>
        <div class=" header-back iconfont icon-star"></div>
        </router-link>
    </div>
</template>
<script>
export default {
    name:"CityHeader"
    
}
</script>
<style scoped>
.header{
    height: .86rem;
    line-height: .86rem;
    overflow: hidden;
    text-align: center;
    color:#fff;
    background-color: steelblue;
    font-size:.32rem;
    position: relative;

}
.header-back{
    color:white;
    font-size:.5rem;
    position: absolute;
    top:0;
    left:0;
    width: .64rem;
    text-align: center;
}

</style>