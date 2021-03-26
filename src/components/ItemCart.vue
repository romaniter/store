<template>
    <div class="cart">
        <div class="block">
            <div class="id left">
              ID: {{item.id}}
            </div>
            <div class="cartimg">
            <img class="img" v-bind:src="item.photo" />
            </div>
            <div class="name center">
              {{item.name}}
            </div> 
            <div class="cost">
              {{item.cost}} р.
            </div>
            <button @click="$emit('addtocart', item.id)" class="btn tocart">
              В корзину
            </button>
        </div>
    </div>
</template>

<script>
import Items from '@/components/Items';

export default {
    name: 'ItemCart',
    components: {
        Items
    },
    props: ['item']
}
</script>

<style scoped>
.cart {
    display: inline-flex;
    width: 250px;
    height: 340px;
    border: solid 1px #CCCCCC;
    border-radius: 3%;
    padding: 20px;
    margin: 5px;
}
.center {
    text-align: center;
}
.left {
    text-align: left;
}
.block {
    display: block;
    position: relative;
    width: 100%;
}
.id {
    font-size: 10px;
    margin-bottom: 10px;
}
.name {
    font-size: 20px;
    position: absolute;
    bottom: 50px;
    left: 1%;
    right: 1%;
}
.cost {
    display: inline;
    position: absolute;
    left: 0px;
    bottom: 0px;
    text-align: left;
}
.btn, .btn:focus {
    background: #a7f330;
    background: linear-gradient(to top, #a7f330, #53d300);
    color: #ffffff;
    font-weight: 700;
    height: 27px;
    width: 100px;
    border: none;
    border-radius: 3px;
    box-shadow: 0px 1px 1px 0px rgba(34, 60, 80, 0.4);
    outline: none;
    cursor: pointer;
}
.btn:hover {
    background: #a7f330;
    background: linear-gradient(to top, #21d310, #01a300);
    cursor: pointer;
}
.tocart {
    display: inline;
    position: absolute;
    right: 0px;
    bottom: 0px;
    height: 27px;
    width: 100px;
}
.cartimg {
    position: absolute;
    width: 200px;
    height: 200px;
    left: 25px;
    top: 0px;
    margin-top: 20px;
}
.img {
    width: 100%;
}
</style>
