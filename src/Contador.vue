<script lang="ts">
    // console.log('Holita');
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
        mounted() {
            console.log('Componente Contador montado '+ this.count)
        }
    }
</script>

<template>
    <h1>Contador: {{ count }}</h1>
    <button @click="increse">Incrementar</button>
    <button @click="decrese">Decrementar</button>
</template>