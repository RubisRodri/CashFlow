<template>
    <div class="splashscreen">
        <img 
            src="@/assets/vector.png"
            alt=logo
        />
        <h1><span>Cash</span>Flow</h1>

    </div>
</template>
<script>
export default{

}


</script>


<style scoped>
.splashscreen {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100vh;
}
h1 {
  color: var(--brand-blue);
}
h1 span {
  color: var(--brand-green);
}
</style>