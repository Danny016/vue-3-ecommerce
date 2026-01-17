<script lang="ts">
    import type { PropType } from 'vue';
    import type { CartDetail } from './types';
    export default {
        props: {
            details: {
                type: Object as PropType<Array<CartDetail>>,
                required: true
            }
        }
    }
</script>

<template>
    <div class="cart">
        <p>Productos agregados al carrito:</p>
        <ul>
            <li v-for="detail in details" :key="detail.productId">
                Producto {{ detail.productId }} - (Qty: {{ detail.quantity }})
            </li>
        </ul>
    </div>
</template>