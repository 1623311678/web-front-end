<template>
  <transition>
    <slot></slot>
  </transition>
</template>
<script>
export default {
  name:'Fade'
  
}
</script>
<style scoped>
.v-enter, .v-leave-to{
  opacity: 0;
}
.v-enter-active, .v-leave-avtive{
  transition: opacity .5s ;
}
</style>


