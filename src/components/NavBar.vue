<template>
  <div
    class="flex justify-evenly bg-emerald-800 p-3  text-white gap-10  w-full"
  >
    <router-link
      to="/"
      class=" my-auto lg:w-7/12"
      >Counter APP</router-link
    >
    <router-link to="/about">
      <button class="bg-white text-emerald-800 px-4 py-1 rounded-lg gap-4">
        About
      </button></router-link
    >
    <router-link to="/counter"
      ><button class="bg-white text-emerald-800 px-4 py-1 rounded-lg">
        Counter
      </button></router-link
    >
  </div>
</template>

<script>
export default {
  name: "NavBar",
  // components: { NavLink,}
  data() {
    return {
      style: {
        li: `text-red-800`,
      },
    };
  },
};
</script>


<style>
#app {
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