<template>
  <div id="bg-ad">
      <div class="container d-flex">
        <div id="box-1" class="container-ad">
            <div class="spacer">
                <div><h3>70% Off</h3></div>
                <div class="text">Vivamus Tempor leo lacus, feugiat ut magna aliquam erat.</div>
            <div class="rounded-pill">View More</div>  
        </div>
            
        </div>
        <div id="box-2" class="container-ad">
            <div class="spacer">
                <div><h3>Free Shipping</h3></div>
                <div class="text">Vivamus Tempor leo lacus, feugiat ut magna aliquam erat.</div>
                <div class="rounded-pill">View More</div>
            </div>

        </div>
      </div>
      
  </div>
</template>

<script>
export default {
    name: 'AdProd',
}
</script>

<style lang='scss' scoped>
#bg-ad{
    margin-top: 40px;
    background-image: url('../../assets/images/bkgd_confetti-compressor.jpg');
    background-position: center;
    background-size: cover;
    height: 400px;
}

#box-1{
    background-image:url('../../assets/images/promo_box_1_bg.jpg') ;
    background-size: cover;
}
#box-2{
    background-image:url('../../assets/images/promo_box_2_bg.jpg') ;
    background-size: cover;
}

.container {
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

.spacer{

height: 100%;
margin-top: 50px;
margin-left: 45px ;
}
.container-ad{
    height: 70%;
    width: 48%;
    color: white;
    h3 {
        font-weight: 600;
        font-size: 44px;
    }

    .text {
        width: 42%;
        margin: 10px 0;
    }

    .rounded-pill {
        border: 2px solid white;
        background-color: rgba(255,255,255, 0.3);
        display: inline-block;
        padding: 5px 15px;
    }
    .rounded-pill:hover {
        background-color: rgba(255,255,255, 0.6);

    }
}
</style>