<template>
  <Suspense>
    <template #default>
      <myHome />
    </template>
    <template #fallback>
      <splash-screen />
    </template>
  </Suspense>


</template>

<script>
import SplashScreen from "@/components/SplashScreen.vue";
//importar componente asincrono para que espere a que se renderize otro
import { defineAsyncComponent } from "vue";
import Layout from "@/components/Layout.vue";

export default {
  components: {
    SplashScreen,
    Layout,
    MyHome: defineAsyncComponent(() => {
      return new Promise((resolve) => {
        setTimeout(() => {
          resolve(import("@/components/MyHome.vue"));
        }, 2500);
      });
    }),
  },
  data() {
    return {
     
    };
  },
};
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
