<template>
<!-- em template eu tenho exatamente o que eu quero mostrar
na minha aplicação -->
 <div>
    <Comp/>
  <h1>Component pai</h1>
  <LifeCycle/>
  <Info/>
 </div>
</template>



// em script eu exporto esse component
<script>

import Comp from './components/comp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Info from './components/info.vue'
  export default {
    name: 'App',
    components:{
      Comp,
      LifeCycle,
      Info
    }
  }
</script>

<style>
  body{
    background-color: aqua;
  }
</style>