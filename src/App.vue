<template>
  <div id="app">
    <transition mode="out-in" enter-active-class="animate__animated animate__zoomIn" leave-active-class="animate__animated animate__zoomOut">
  <router-view/>
  </transition>
  </div>
</template>
<script>

export default {
 components:{
      
  }
 }
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=IBM+Plex+Sans");


#banner{
  min-height: 100vh;
}


</style>
