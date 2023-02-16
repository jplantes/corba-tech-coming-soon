<template>
  <div class="grid grid-flow-col gap-5 text-center auto-cols-max">
    <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
      <span class="countdown font-mono text-5xl">
        <span :style="{'--value':dias}"></span>
      </span>
      Días
    </div> 
    <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
      <span class="countdown font-mono text-5xl">
        <span :style="{'--value':horas}"></span>
      </span>
      Horas
    </div> 
    <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
      <span class="countdown font-mono text-5xl">
        <span :style="{'--value':min}"></span>
      </span>
      min
    </div> 
    <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
      <span class="countdown font-mono text-5xl">
        <span :style="{'--value':seg}"></span>
      </span>
      seg
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    
    const dias = ref()
    const horas = ref()
    const min = ref()
    const seg = ref()


    const resta = () => {
      const fecha1 = new Date('2023/03/01');
      const fecha2 = new Date()

      const resta2 = new Date( fecha1 - fecha2 )


      dias.value = Math.round(resta2/ (1000*60*60*24))
      horas.value = resta2.getHours()
      min.value = resta2.getMinutes()
      seg.value = resta2.getSeconds()
    }
    
    setInterval( () => {
      resta()
    }, 1000 )


    return {
      dias,
      horas,
      min,
      seg,
    }
  }
}
</script>
