<template>

<Suspense>
  <template #default>
    <MyHome />
  </template>
  <template #fallback>
    <splash-screen/>
  </template>

</Suspense>


  
</template>

<script>
import SplashScreen from "@/components/SplashScreen.vue";
//importar componente asincrono para que espere a que se renderize otro
import { defineAsyncComponent } from "vue";
import MyHome from '@/components/MyHome.vue';

export default {
  components:{
    SplashScreen,
    MyHome: defineAsyncComponent(() =>{
       return new Promise((resolve) => {
        setTimeout(() => {
          resolve(import("@/components/MyHome.vue"))
        }, 2500);
      })
    }),
  }
}

</script>

<style>
.app {
  min-height: 100vh;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
* {
  --brand-green: #04b500;
  --brand-blue: #0689b0;
}
</style>
