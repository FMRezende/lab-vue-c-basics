<template lang="">
    <div :class="[backgroundColor]">
        <button @click="changeColor">Change Color</button>
        <h1>My box dynamic color!</h1>
    </div>
</template>

<script>
import { ref } from 'vue'
export default {
     data() {
        return {
            backgroundColor: ref('orange')
        }
     },
    methods: {
        changeColor (){
            this.backgroundColor = this.backgroundColor === 'orange' ? 'purple' : 'orange';
        }
    },
}
</script>

<style lang="css">
   .orange {
    background-color: orange
   }
   .purple {
    background-color: purple
   }
</style>