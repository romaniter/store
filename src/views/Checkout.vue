<template>
    <div>
       <Cart
       v-for="cart of globalCarts"
       v-bind:cart="cart"
       /> 
    </div>
</template>

<script>
import Cart from '@/components/Cart';
import Items from '@/components/Items';

export default {
    name: "Checkout",
    props: ["globalCarts"],
    components: {
        Cart,
        Items
    },
    props: ["carts"]
}
</script>
