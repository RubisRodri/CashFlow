<template>
    <header>
        <img 
        @click="reload"
        src="@/assets/vector.png" 
        alt="logo"
        />
    <h1><span>CashF</span>loat</h1>
    <span></span>
    </header>
</template>

<script>
export default{
    methods:{
        reload(){
            loca.reload();
        }
    }
}
</script>
<style scoped>

</style>