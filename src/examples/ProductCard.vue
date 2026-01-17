<script lang="ts">
import type { Product } from './Product';
import type { PropType } from 'vue';
    export default {
        props: {
            product: {
                type: Object as PropType<Product>,
                required: true
            }
        },
        emits: ['addProduct'],
        methods: {
            onAddButtonClick() {
                this.$emit('addProduct');
            }
        }
    }
</script>

<template>
    <div class="product-card">
        <p>Producto: {{ product.name }}</p>
        <p>Precio: ${{ product.price }}</p>
        <button @click="onAddButtonClick">Agregar al carrito</button>
        <hr/>
    </div>
</template>