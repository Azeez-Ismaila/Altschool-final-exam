<template>
  <div class="home flex flex-col gap-4">
    <div>
      <h1>Hello Welcome to My Counter App Created with VUE</h1>
    </div>
   
    <div>
     Counter app with Vuejs that performs increment, decrement, reset and setVaue functions, using Vuex as state management
    </div>
    <div class="link">
    <div><RouterLink to="/counter"><button class="bg-emerald-800 text-white px-4 py-1 rounded-lg">
        Counter
      </button></RouterLink> </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  // name: 'HomePage',
  components: {
    // HelloWorld
  }
}
</script>
