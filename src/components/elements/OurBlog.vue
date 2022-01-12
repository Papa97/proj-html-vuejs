<template>
    <div>
    <div class="container">
        <div class="text-center">
            <div class="new-arrivals" > 
                <h2>Our Blog</h2> 
            </div>
            <hr class="hr-1">
            <hr class="hr-2">
            <div class="light">The latest Classic Shop News</div>
        </div>


        <div class="row">
            <div class="col" v-for="(post, index) in posts" :key="index">
                <div>
                    <img :src="require('../../assets/images/' + post.img)" alt="">
                </div>
                <div class="titolo">
                    {{post.titolo}}
                </div>
                <div class="date">
                    {{post.data}}
                </div>
                <div class="sotto-titolo">
                    {{post.sottoTitolo}}
                </div>
            </div>
        </div>
    </div>
    <hr>
    </div>
</template>

<script>
export default {
    name: 'OurBlog',
    props : {
        posts : Array
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

.row{
    margin-bottom: 100px;
    img{
        width:100%
    }
}

.titolo {
    font-weight: 600;
}

.date,
.sotto-titolo {
    font-size: 14px;
}

.date{
    margin: 5px 0 15px
}
</style>