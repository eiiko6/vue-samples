<script setup>
  import Navbar from './components/transparent-navbar/Navbar.vue'
</script>

<template>
  <Navbar />
  <div class="background"></div>
</template>

<style scoped>
  .background {
        z-index: -1;
        margin: 0;
        padding: 0;
        top:0px;
        right:0px;
        bottom:0px;
        left:0px;
        background: url(./assets/snowfall-201496.jpg) no-repeat center center fixed; 
        -webkit-background-size: cover;
        -moz-background-size: cover;
        -o-background-size: cover;
        background-size: cover;
        filter: blur(0px) opacity(0.5);
        height: 250vh; /*Adjust manually*/
        position: fixed;
        min-height: 100%;
        height: auto;
    }
</style>
