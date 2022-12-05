<template>
  <div>
       <AA :renwu="renwu"></AA>
       <BB :parent="renwu"></BB>
       <CC :renwu="renwu"></CC>
     
  </div>
</template>

<script>
 import { reactive } from '@vue/runtime-core'

import AA from './components/aa.vue'
import BB from './components/bb.vue'
import CC from './components/cc.vue'
  export default{
       components:{
         AA,
         BB,
         CC
       },
     setup(){
        let renwu=reactive([
          {cc:'开会',completed:false},
           {cc:'吃饭',completed:true},
          {cc:'出差',completed:true},
           {cc:'约会',completed:true}
          ])
        return{
           renwu
          
        }
     }
  }

 
   
  
</script>

<style>

</style>
