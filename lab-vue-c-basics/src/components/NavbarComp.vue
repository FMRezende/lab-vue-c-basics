<template lang="">
    <div>
        <h2 v-show="showNavbar">Navbar</h2>
        <button @click="toggleShowMensaje">Mostrar/Ocultar mensaje</button>
    </div>
</template>

<script>
export default {
    data(){
        return {
            showNavbar: true,
        }
    },
    methods: {
        toggleShowMensaje (){
            this.showNavbar = !this.showNavbar
        }
    }
}
</script>

<style lang=""> 
</style>