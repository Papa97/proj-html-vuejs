<template>
    <div class="header-top container">
        <div>
            <ul class="general-menu">
                <li class="header-top__fonts"><i class="fab fa-facebook-f"></i></li>
                <li class="header-top__fonts"><i class="fab fa-twitter"></i></li>
                <li class="header-top__fonts"><i class="fab fa-instagram"></i></li>
                <li class="header-top__fonts"><i class="fab fa-youtube"></i></li>
            </ul>
        </div>
      

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
      <hr>
    </div>
</template>

<script>
export default {
    name:'HeaderTop',
}
</script>

<style lang="scss" scoped>

.header-top{
  display: flex;
  justify-content: space-between;
  font-size: 12px;
  color:#6b6a6b;
}

.piccolo{
    font-size:8px;
}
.general-menu {
    display: flex;
    list-style: none;
    margin: 0;
    
    li{
        padding:10px 5px
    }
    .last-li{
        border-right: none;
        padding: 10px 40px;
        text-transform: uppercase;
        span {
            margin: 0 10px;
        }
    }
    span{
        padding:10px 0
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