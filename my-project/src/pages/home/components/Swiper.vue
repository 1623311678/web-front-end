<template>
    <div class="wrapper">
        <swiper :options="swiperOption" v-if="showSwiper">
    <swiper-slide v-for="item in list" :key="item.id">
      <img class="swipe-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
    </div>
</template>
<script>
export default {
    name:'HomeSwiper',
    props:{
        list: Array
        
    },
    data () {
        return{
            swiperOption: {
            pagination: '.swiper-paginatio',
            loop: true  
        }
       
        }
    },
    computed: {
        showSwiper () {
            return this.list.length
        }
    }
    
}
</script>
<style scoped>
 
.wrapper{
    overflow:hidden;
    width: 100%;
    height: 0;
    padding-bottom:26%;
}

.swipe-img{
    width:100%;

}

</style>


