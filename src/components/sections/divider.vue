<template>
    <div class="container text-center">
        <div class="best-seller" > 
            <h2>Best Seller</h2> 
        </div>
        <hr class="hr-1">
        <hr class="hr-2">
    </div>
</template>

<script>
export default {
    name:'divider',
    props: {

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
</style>