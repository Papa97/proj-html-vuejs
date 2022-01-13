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
                <div class="maschera">
                    <div class="overlay">
                        <div class="overlay__center">
                            <div>{{prod.title}}</div>
                            <div>{{prod.desc}}</div>
                            <div>{{prod.prize}}</div>
                        </div>
                        <div class="overlay__bottom">
                            <div><i class="fas fa-shopping-cart"></i> Add to cart</div>
                            <div><i class="fas fa-list-ul"></i> Details</div>
                        </div>
                    </div>
                    <img :src="require('../../assets/images/' + prod.img)" alt="">
                </div>
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

.maschera {
    position: relative;
}

.overlay {
    position: absolute;
    font-weight:600;
    color: #fff;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, 0);
    z-index: 1000;
    display: none;
    width: 100%;
    &__bottom {
        margin-top: 100px;
        display: flex;
        justify-content: space-between;
        bottom: 0;
        padding: 0 10px ;
    }
}

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
        // height: 300px;
        width: 100%;
    }
}

.product-best:hover {
    background: rgb(66,126,213);
    background: linear-gradient(180deg, rgba(66,126,213,0.9023984593837535) 0%, rgba(226,128,177,0.9023984593837535) 100%);
    img {
        opacity: .3;
    }
    .overlay {
        display: block;
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
    z-index: 20000;
}
.chev-right{
    right: 0;
}

</style>