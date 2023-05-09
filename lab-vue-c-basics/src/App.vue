<template>
  <navbarComp></navbarComp>
  <h1>Operation result 2 + 2 es: {{ 2 + 2 }} </h1>
  <h1>{{ textoGenerado }}</h1>
  <BackgroundColor></BackgroundColor>
  <FooterComp></FooterComp>
</template>


<script>
import NavbarComp from './components/NavbarComp.vue'
import FooterComp from './components/FooterComp.vue'
import BackgroundColor from './components/BackgroundColor.vue'
export default {
  name: 'App',
  data() {
    return {
      nombre: "Felipe",
      apellido: "Rezende",
      edad: 42,
    }
  },
  computed: {
    textoGenerado(){
      return `Hola, mi nombre es ${this.nombre} ${this.apellido} y tengo ${this.edad} años.`
    }
  },
  components: {
    NavbarComp,
    FooterComp,
    BackgroundColor
}
}
</script>


<style scoped>
</style>