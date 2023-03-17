<template>
  <h1 className="text-emerald-800">A VUE Counter APP</h1>
  <span class="font-extrabold lg:text-8xl  text-emerald-800">Count is: {{ count }}</span>
  <!-- <span class="font-extrabold text-9xl text-emerald-800">{{ countInput }}</span> -->
  

    <input type="number" :value="countInput" @change="updateInput" @keyup.enter="setValue" class="border-emerald-800 border-4 rounded-md lg:w-5/12 w-10/12 mx-auto"/>
  <div class="flex justify-evenly lg:justify-center lg:gap-6 text-white">
    <button @click="decrement" class="rounded-lg p-3 bg-emerald-800">Decrement</button>
    <button @click="reset" class="rounded-lg p-3 bg-emerald-800">Reset</button>
    <button @click="increment" class="rounded-lg p-3 bg-emerald-800">Increment</button>
  </div>
  <button @click="setValue" class="rounded-lg p-3 bg-emerald-800 w-5/12 mx-auto text-white">Set Count</button>
</template>

<script>
// import counter from '../composables/counter'

// import { mapState, mapActions } from "vuex";

// export default {
  // setup() {
  //     const { count, increment, decrement, reset} = counter()

  //     return {count, increment, decrement, reset}
  // }


//   computed: {
//     ...mapState({
//       count: (state) => state.defaultCount,
//       countInput: (state) => state.form.count,
//     }),
//   },
//   methods: {
//     ...mapActions([
//         'increment',
//         'decrement',
//         'reset'
//     ]),
   
//     updateInput(e) {
//         if (!this.$store.state.form.count) { 
//              e.preventDefault()
//             this.$store.dispatch("updateInput", e.target.value);
//         } else {
//             console.log('not an empty string');
//         }
//         },
//     setValue() {
//         if (this.$store.state.form.count) {
//             this.$store.dispatch('setValue', this.countInput)
//             this.$store.state.form.count = ''
//             console.log('input accessed');
//         } else {
//             console.log('input clicked');
//         }
        
//     },
    
//   },

// };
   import {computed } from 'vue';
   import {useStore} from 'vuex';


    export default {
      setup () {
        const store = useStore();

        return {
          // accessing states
          count: computed(() => store.state.defaultCount),
          countInput: computed(() => store.state.form.count),
          // accessing actions
          increment: () => store.dispatch('increment'),
          decrement: () => store.dispatch('decrement'),
           reset: () => store.dispatch('reset'),
          updateInput: (e) => {
              if (!store.state.form.count) {
                       e.preventDefault() 
                      store.dispatch("updateInput", e.target.value);
                      console.log('input updated');
              } else {
                      console.log('not an empty string');
                  }
          },
          setValue: () => {
                if (store.state.form.count) {
                    store.dispatch('setValue', store.state.form.count)
                    store.state.form.count = ''
                    console.log('input accessed');
                } else {
                    console.log('input clicked');
                }

            },
        }
        
      }
    }




</script>



