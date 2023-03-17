<template>

  <div
      class="text-white bg-emerald-800 text-center p-4 block w-screen bottom-0 text-xl"
    >
      © 2022 Copyright: Powered By Zyzman
    </div>
</template>

<script>
// import NavLink from './components/NavLink.vue';

export default {
  name: 'FooterPage',
  // components: { NavLink,}
  data() {
    return {
      style: {
        li: `text-red-800`
      }
    }
  }

}
</script>


<style> #app {
   font-family: Avenir, Helvetica, Arial, sans-serif;
   -webkit-font-smoothing: antialiased;
   -moz-osx-font-smoothing: grayscale;
   text-align: center;
   color: #2c3e50;
 }

 #nav {
   padding: 30px;
 }

 #nav a {
   font-weight: bold;
   color: #2c3e50;
 }

 #nav a.router-link-exact-active {
   color: #42b983;
 }
</style>