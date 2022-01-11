<template>
    <div class="container">
        <div class="d-flex justify-content-between w-100 h-100 align-items-center">
            <div><img src="../../assets/images/classic_shop_logo2x.png" alt=""></div>
            <div class="nav-bar-head h-100">
                <ul class="h-100 d-flex">
                    <li class="general-link h-100" v-for="(link ,index) in links" :key='index'>
                        <a href="#">{{link.testo}}
                        <span v-if="link.chevron == true"><i class="fas fa-chevron-down piccolo"></i></span>
                        </a>
                    </li>
                    <a href="#"><li class="rounded-pill "> Shop Now! </li></a>
                    <a href="#"><li><i class="fas fa-search dark"></i></li></a>
                </ul>
            </div>
        </div>  
    </div>
</template>

<script>
export default {
    name: 'navBar',
    props: {
        links: Array,
    }
}
</script>

<style lang="scss" scoped>
.container{
    position: relative;
    box-sizing: border-box;
    // margin-bottom: 40px;
    height: 152px;
    display: flex;
    width: 100%;
    justify-content: space-between;
    align-items: center;
}
img {
    width: 200px;
}
.rounded-pill {
    background-color: #427ed5;
    text-transform: uppercase;
    color: #fff;
    font-weight: 700;
    padding: 10px 20px;
}
.nav-bar-head{
    ul {
        list-style: none;
        font-size: 12px;
        
    }
}

.general-link{
    box-sizing: border-box;
    align-self: center;
    display: flex;
    padding: 0 15px;
    border-top:2px solid transparent ;
}

.general-link,
a{
    color: #6b6a6b;
    text-decoration: none;

}



.general-link:hover{
    border-top: 2px solid #427ed5;
    color:#427ed5

}

.piccolo{
    font-size:8px;
}

.dark {
    color:#2a2f33 ;
    margin-left: 10px;
    &:hover{
        color: #427ed5;
    }
}

ul {
    a {
        align-self: center;
    }
}
</style>   