<template>
    <div>
        <div class="container text-center">
            <div class="new-arrivals" > 
                <h2>New Arrivals</h2> 
            </div>
            <hr class="hr-1">
            <hr class="hr-2">
            <div class="light">Must have products from our top sellers</div>
        </div>

        <div class="container-prod">
            <div class="chev-left"><i class="fas fa-chevron-left"></i></div>
            <div class="product-best" v-for="(arrival, index) in arrivals" :key="index">
                <img :src="require('../../assets/images/' + arrival)" alt="">
            </div>
            <div class="chev-right"> <i class="fas fa-chevron-right"></i></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NewArrivals',
    props: {
        arrivals : Array
    }
}
</script>

<style lang='scss' scoped>
.container{
    position: relative;
    margin-top: 80px;
}

.new-arrivals{
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
    margin: 50px 0;
    display: flex;
    position: relative;
    width: 100%;
    overflow-y:hidden ;
}
.product-best{
    width: calc(100%/5);
    cursor: pointer;
    text-align: center;

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