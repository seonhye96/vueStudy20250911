<template>
  <div>
    <p>{{ message }}</p>
    <button @click="changeMessage">chage</button>
  </div>
</template>

<script>
// import { ref } from 'vue';
import { useMessage } from './hooks/useMessage'

  export default {
    /** step1 */
    // data() {
    //   return {
    //     message: 'hello'
    //   }
    // },
    // methods: {
    //   changeMessage(){
    //     this.message='hi'
    //   }
    // }

    /** step2 */
    setup(){
        /** step3 */
        const { message , changeMessage } = useMessage();
      // // data
      // const message = ref('hello');

      // //methods
      // function changeMessage(){
      //   message.value = 'hi';
      // }

      return {message , changeMessage}
    }
  }
</script>

<style lang="scss" scoped>

</style>