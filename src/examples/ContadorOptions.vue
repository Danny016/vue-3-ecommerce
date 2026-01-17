<script lang="ts">
    export default {
        data() {
            return {
                count: 0
            };
        },
        methods: {
            increse() {
                this.count++;
            },
            decrese() {
                this.count--;
            }
        },
        mounted(){
            console.log('Componente Contador montado '+ this.count);
        }
    }
</script>

<template>
    <p>Objeto: Tienes que llegar a 10 clicks</p>
    <h1>Contador: {{ count }}</h1>
    <button @click="increse">Incrementar</button>
    <button @click="decrese">Decrementar</button>
    <p v-if="count <= 10">Vamos tu puedes!</p>
    <p v-else>Lo lograste!</p>
</template>