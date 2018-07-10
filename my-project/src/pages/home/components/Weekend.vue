<template>
    <div>
        <div class="recommend-title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom " v-for="item in list" :key="item.id">
                    <div class="item-img-wrapper">
                    <img class="item-img" 
                     :src="item.imgUrl">
                    </div>
                <div class="item-info">
                    <p class="item-title">{{item.item}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name:'HomeWeekend',
    props:{
        list:Array
    }
    
}

</script>
<style scoped>
.recommend-title{
    line-height: .8rem;
    background: #eee;
    margin-top:.2rem;
    text-indent:.2rem   
}
.item-img-wrapper{
    height:0;
    overflow: hidden;
    padding-bottom:33.9%;
}

.item-img{
    width: 100%;
   
}
.item-info{
    padding:.1rem;
}
.item-title{
    line-height: .54rem;
    font-size:.32rem;
}
.item-desc{
    line-height: .4rem;
    color:#ccc;
}


</style>

