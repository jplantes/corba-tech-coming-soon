<template>
  <div class="flex flex-col-reverse md:flex-row h-screen">
    
    <div class="md:basis-1/2 flex flex-col h-2/3 md:min-h-full items-center justify-center bg-white">
      <h1 class="text-4xl md:text-5xl mb-5 text-center">Sitio en construcción</h1>
      <h4 class="text-2xl mb-1">Software Factory</h4>
      <h4 class="text-2xl mb-10">Aplicaciones Web & Mobile</h4>
      <Decrement />
    </div>

    <div class="md:basis-1/2 flex bg-gray-700 h-1/3 md:min-h-full items-center justify-center">
      <img class="min-w-md" src="./assets/corba-negro.png" alt="">
    </div>

  </div>
</template>

<script>
import Decrement from './components/Decrement.vue';



export default {
  components:{
    Decrement
  },

  setup () {

    return {}
  }
}
</script>

<style scoped>

</style>