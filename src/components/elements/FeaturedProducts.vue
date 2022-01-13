<template>
    <div class="container">
      <div class="text-center">
        <div class="featured-products" > 
            <h2>Featured Products</h2> 
        </div>
        <hr class="hr-1">
        <hr class="hr-2">
        <div class="light">Must have products from our top sellers</div>

        <div>
            <ul class="d-flex menu">
                <li>Men</li>
                <li>Women</li>
                <li>Accessories</li>
            </ul>
        </div>
        <div class="row">
            <div class="col-3" v-for="(desc, index) in feat" :key="index">
                <div><img :src="require('../../assets/images/' + desc.img)"></div>
                <p class="feat-name">{{ desc.descrizione }}</p>
                <p class="feat-desc">{{ desc.keyWord}}</p>
                <p class="prezzi">
                    <span v-if="desc.prezzoListino" class="wrong" >${{desc.prezzoListino}} </span>
                    <span> ${{desc.prezzoSconto}}</span></p>
            </div>

        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'FeaturedProducts',
    props: {
        feat: Array,
    }
}
</script>

<style lang="scss" scoped>

.feat-name,
.feat-desc,
.prezzi {
    text-align: left;
}

.feat-name{
    font-weight: 600;
    margin-top: 30px;
}
.container{
    margin-top: 30px;
    position: relative;
}

.col-3{
    margin-bottom: 80px;
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

.featured-products{
    background-color: #fff;
    display: inline-block;
    h2{
        font-weight: 600;
    }
}

.light{
    color: #6b6a6b;
}

.menu{
    margin-top: 30px;
    justify-content: center;
    font-weight: 600;
    li{
        list-style: none;
        padding: 10px 40px;
        border: 1px solid #ececec;
        background-color:#f0f0f0 ;
    }
    li:hover {
        background-color: #fff;
    }
}

.prezzi {
    color:#427ed6;
}

.wrong{
    text-decoration: line-through;
    font-size: 14px;
}
</style>