<template>
    <div class="container">
        <div class="header-top">
            <div>
                <ul class="general-menu-social">
                    <li class="header-top__fonts"><i class="fab fa-facebook-f"></i></li>
                    <li class="header-top__fonts"><i class="fab fa-twitter"></i></li>
                    <li class="header-top__fonts"><i class="fab fa-instagram"></i></li>
                    <li class="header-top__fonts"><i class="fab fa-youtube"></i></li>
                </ul>
            </div>
        
        <div class="prova">
        <div class="right-top d-flex">
            <ul class="general-menu">
                <li>Shopping Cart</li>
                <li class="border-head">
                    My Account
                    <i class="fas fa-chevron-down piccolo"></i>
                </li>
                <li class="last-li">
                    <i class="fas fa-shopping-cart"></i>
                    <span>Cart</span>
                    <i class="fas fa-chevron-down"></i>
                </li>
            </ul>
            
        </div>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'HeaderTop',
}
</script>

<style lang="scss" scoped>
.general-menu-social{
    display: flex;
    list-style: none;
    padding-left: 0;
    li {
        padding:0px 15px 0px 0;
    }
}

.header-top{
  display: flex;
  justify-content: space-between;
  font-size: 12px;
  color:#6b6a6b;
  height: 75px;
  line-height: 75px;
}

.piccolo{
    font-size:8px;
}
.general-menu {
    display: flex;
    list-style: none;
    margin: 0;
    padding-left: 0;
    li{
        padding:0 25px
    }
    .last-li{
        background-color: #f0f0f0;
        border-right: none;
        padding: 0 80px;
        text-transform: uppercase;
        span {
            margin: 0 10px;
        }
    }
}


.border-head {
    border-top: 0;
    border-bottom: 0 ;
    border-left:1px solid;
    border-right: 1px solid;
    border-color: #eee;
}
</style>