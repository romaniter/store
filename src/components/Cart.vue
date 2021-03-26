<template>
    <div>
        Корзина
        {{cart}}
    </div>
</template>

<script>
import Checkout from '@/views/Checkout'

export default {
    name: "Cart",
    components: {
        Checkout
    },
    props: ["cart"]
}
</script>

<style scoped>
    
</style>
