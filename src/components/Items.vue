<template>
    <div class="items">
        <ItemCart
        v-for="item of items"
        v-bind:item="item"
        v-bind:key="item.id"
        v-on:addtocart="toCart"
        />
    </div>
</template>

<script>
import ItemCart from '@/components/ItemCart'

export default {
    name: 'Items',
    components: {
        ItemCart
    },
    data() {
        return {
            items: [
                {id: 1, name: 'Товар 1', cost: 1000, photo: 'https://picsum.photos/300/200'},
                {id: 2, name: 'Товар 2', cost: 4500, photo: 'https://picsum.photos/240'},
                {id: 3, name: 'Товар обыкновенный в единичном экземпляре', cost: 1600, photo: 'https://picsum.photos/230'},
                {id: 4, name: 'Товар 4', cost: 6700, photo: 'https://picsum.photos/250'},
                {id: 5, name: 'Товар 5', cost: 10400, photo: 'https://picsum.photos/210'},
                {id: 23, name: 'Универсальный товар', cost: 1000, photo: 'https://picsum.photos/300/200'},
                {id: 22, name: 'Товар который нужен всем', cost: 4500, photo: 'https://picsum.photos/240'},
                {id: 31, name: 'Товар обыкновенный в единичном экземпляре', cost: 1600, photo: 'https://picsum.photos/230'},
                {id: 41, name: 'Товар 44546', cost: 6700, photo: 'https://picsum.photos/250'},
                {id: 53, name: 'Кирпич красный', cost: 10400, photo: 'https://picsum.photos/210'}
            ]
        }
    },
    methods: {
        toCart(id) {
            this.$emit.$globalCarts.push(this.items[id]);
        }
    },
}
</script>

<style scoped>
.items {
    display: initial;
    width: 80%;
}
</style>
