<template>
    <div class="container">
        <div class="d-flex justify-content-between">
            <div><img src="../../assets/images/classic_shop_logo2x.png" alt=""></div>
            <div class="nav-bar-head">
                <ul class="d-flex">
                    <li class="general-link" v-for="(link ,index) in links" :key='index'>
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
    margin-bottom: 40px;
}
img {
    width: 200px;
    margin-top: 30px;
}
.rounded-pill {
    background-color: #427ed5;
    text-transform: uppercase;
    color: #fff;
    font-weight: 700;
    padding: 10px 20px;
    margin-top: 30px;
}
.nav-bar-head{
    ul {
        list-style: none;
        font-size: 12px;
        
    }
}

.general-link{
    padding: 40px 20px 0;
    box-sizing: border-box;
}

// .general-link,
// li:last-of-type{
//     padding: 10px 15px
// }


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
    margin-top: 40px;
    margin-left: 10px;
    &:hover{
        color: #427ed5;
    }
}

</style>   