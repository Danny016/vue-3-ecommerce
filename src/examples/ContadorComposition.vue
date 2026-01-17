<script setup lang="ts">
    import {onMounted, ref} from 'vue';
    const contador =ref(0);
    function incrementar(){
        contador.value++;
    }
    onMounted(function() {
        console.log('El valor del contador es: '+ contador.value);
    });
</script>

<template>
    <p>hla soy la version con Composition API</p>
    <h1>Contador: {{ contador }}</h1>
    <button @click="incrementar">Incrementar</button>
</template>