<template>



<div style="color:white">
  <br><br>

{{$q.screen}}

</div>

<div class="q-pa-md">
    <q-img
      src="../../public/img/titulo.png "
      img-class="my-custom-image"
      class="rounded-borders borders xl:w-[20rem] md:left-[0rem] md:w-[22rem] 2xl:left-[6rem] 2xl:top-[9rem] xl:top-[8rem] " 
    >
      
    </q-img>
  </div>


  <div class="q-pa-md">
    <q-img
      src="../../public/img/texto.png "
     
      style=" max-width: 320px"
      img-class="my-custom-image"
      class="rounded-borders 2xl:left-[6rem]   2xl:top-[9rem]  xl:top-[7rem]" 
    >
      
    </q-img>
  </div>





 <div class="q-pa-md">
    <q-img
      src="../../public/img/logo.png "
     
      img-class="my-custom-image"
      class="rounded-borders relative  w-[18rem] 2xl:w-[24rem]  md:w-[18rem] md:left-[64rem] md:top-[-4rem] 2xl:left-[92rem] " 
    >
      
    </q-img>
  </div>


<div class="q-pa-md fixed-center  relative top-[28rem]  xl:top-[22rem] xl:w-[45rem]   2xl:w-[60rem]" transparent	 style=" background-color:black;   opacity: .9;">
   
   
  <div class="row justify-center m-4  q-gutter-sm">
   <div class="col">
      <q-item >
            <p  style="color:white; position:absolute" class=" fixed-center  w-[18rem] xl:w-[40rem]   xl:text-lg " > LA NUEVA VISIÓN DE LA INDUSTRIA TRAE CONSIGO MUCHAS SORPRESAS</p>
      </q-item>   
     </div>  

  </div>

  <q-form class="relative top-4"  @submit="proceso" >
    <q-list bordered>
      <div class="q-pa-md">
        
        <div class="q-gutter-md" >

         <q-input rounded outlined label-color="white"  color="blue"  v-model="name" label="Nombre" />

         <!-- <q-input rounded outlined label-color="white"  color="blue"  v-model="last_name" label="Apellido" />
         <q-input rounded outlined label-color="white" type="email"  color="blue"  v-model="email" label="Email" />
         <q-input rounded outlined label-color="white"   color="blue"  v-model="phone" label="Telefono" />

         <div class="row">

          <q-input class="col-6 " rounded outlined label-color="white"   color="blue"  v-model="coutry" label="Pais" />
          <q-input class="col-6 " rounded outlined label-color="white"   color="blue"  v-model="city" label="Ciudad" />

         </div>

          <q-input class="col-6 " rounded outlined label-color="white" color="blue"  v-model="rol" label="Rol" />
          <q-input class="col-6 " rounded outlined label-color="white" color="blue"  v-model="company" label="Company" /> -->
      
    </div>


            <q-btn class="relative my-3 justify-items-center items-end" type="submit" unelevated rounded color="primary" label="INSCRIBIRME" />

  </div>

     


     
    </q-list>
   </q-form>


   <div class="q-pa-md gt-xs inline">
    <q-img
      src="../../public/img/slogan.png "
     
      style=" max-width: 160px"
      img-class="my-custom-image"
      class="rounded-borders absolute xl:left-[-18rem]  xl:top-[35rem]   2xl:left-[-15rem]  " 
    >
      
    </q-img>
  </div>


  <q-btn-group rounded class="q-pa-md relative   xs:left-[2rem] md:left-[42rem] 2xl:left-[64rem]   "  >
    <q-avatar><img src="../../public/img/tiktok.png"></q-avatar>
    <q-avatar><img src="../../public/img/youtube.png"></q-avatar>
      <q-avatar><img src="../../public/img/facebook.png"></q-avatar>
      <q-avatar><img src="../../public/img/instagram.png"></q-avatar>
      <q-avatar><img src="../../public/img/twitter.png"></q-avatar>
    </q-btn-group>


  </div>
</template>

<style scoped>
 
</style>

<script>
import { defineComponent } from 'vue'
import { useQuasar } from 'quasar'
import { ref } from 'vue'

 

 function setup(){
   
   const $q = useQuasar()
   const name = ref('')

  

    return {
      name,

      onSubmit () {
        if (name.value == null) {
          $q.notify({
            color: 'red-5',
            textColor: 'white',
            icon: 'warning',
            message: 'You need to accept the license and terms first'
          })

          console.log(name)
        }
        else {
          $q.notify({
            color: 'green-4',
            textColor: 'white',
            icon: 'cloud_done',
            message: 'Submitted'
          })
        }
      },

      onReset () {
        name.value = null
        
      }
    }
  }




export default defineComponent({
  name: 'IndexPage'  
  
})
</script>
