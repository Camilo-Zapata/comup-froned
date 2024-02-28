<template>
    <div class="q-pa-md fixed-center"  style="width: 1250px; background-color:black;">
   
   
  <div class="row justify-center">
   <div class="col-12">
      <q-item v-ripple>
            <p style="color:white; font-size:large  " class=" fixed-center" > LA NUEVA VISIÓN DE LA INDUSTRIA TRAE CONSIGO MUCHAS SORPRESAS</p>
      </q-item>   
     </div>  

  </div>

   
    <q-list bordered>


     
      <q-separator />



  <div class="col-12  " >
      <q-item>
          <q-input rounded color="lime-11" bg-color="green" filled v-model="text" label="Label"> </q-input>
      </q-item>
        
  </div>
     

     


     
    </q-list>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
