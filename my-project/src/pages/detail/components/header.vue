<template>
<div>
    <router-link
    tag="div"
    to="/"
    class="header-abs"
    v-show="showAbs"
    >返回 </router-link>
     <div class="header-fixed" v-show="!showAbs" :style="opacityStyle" >景点详情</div>
 
</div>
    
</template>
<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>
<style scoped>



.header-abs{
    position: absolute;
    color:white;
    text-align: center;
    line-height: .8rem;
    left:.2rem;
    top:.2rem;
    width: .8rem;
    height: .8rem;
    border-radius:.4rem;
    background: rgba(0,0,0,.8)
}
.header-fixed{
    position:relative;
    height: 1.2rem;
    line-height: 1.2rem;
    overflow: hidden;
    text-align: center;
    color:#fff;
    background-color: steelblue;
    font-size:.32rem;
    top:-4.2rem;
   
}
</style>

