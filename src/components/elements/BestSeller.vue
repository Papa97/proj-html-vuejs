<template>
    <div class="container text-center">
        <div class="best-seller" > 
            <h2>Best Seller</h2> 
        </div>
        <hr class="hr-1">
        <hr class="hr-2">
        <div class="light">Must have products from our top sellers</div>

        <div class="container-prod">
            <div class="chev-left"><i class="fas fa-chevron-left"></i></div>
            <div class="product-best" v-for="(prod, index) in prods" :key="index">
                <img :src="require('../../assets/images/' + prod)" alt="">
            </div>
            <div class="chev-right"> <i class="fas fa-chevron-right"></i></div>

        </div>
    </div>
</template>

<script>
export default {
    name:'BestSeller',
    props: {
        prods : Array
    }
}
</script>

<style lang='scss' scoped>
.container{
    position: relative;
}

.best-seller{
    background-color: #fff;
    display: inline-block;
    h2{
        font-weight: 600;
    }
}
.hr-1,
.hr-2{
    position: absolute;
    top: 4px;
    width: 37%;
}
.hr-1{
    left:20px;
}
.hr-2{
    right: 20px;
}

.light{
    color: #6b6a6b;
}
.container-prod{
    display: flex;
    position: relative;
}

.product-best{
    width: calc(100%/5);
    cursor: pointer;
    img {
        height: 300px;
    }
}

.chev-left,
.chev-right{
    position: absolute;
    top: 50%;
    transform: translate(0,-50%);
    color: white;
    background-color: #a0a5a5;
    padding: 15px 5px;
}
.chev-right{
    right: 0;
}

</style>