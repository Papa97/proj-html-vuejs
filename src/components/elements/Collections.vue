<template>
  <div class="container-fluid row">
      <div class="col-4" id="winter">
          <div class="container-txt">
            <div><h3>Winter Collections</h3></div>
            <div class="desc">Stylish and Warm</div>
            <a href="#"><div class="rounded-pill">View More</div></a>
          </div>
      </div>
      <div class="col-4" id="spring">
          <div class="container-txt">
            <div><h3>Spring Collections</h3></div>
            <div class="desc">Bright and Colorful</div>
            <a href="#"><div class="rounded-pill">View More</div></a>
          </div>
      </div>
      <div class="col-4" id="autumn">
          <div class="container-txt">
            <div><h3>Autumn Collection</h3></div>
            <div class="desc">Rich and comfortable</div>
            <a href="#"><div class="rounded-pill">View More</div></a>
          </div>
      </div>
  </div>
</template>

<script>
export default {
name:'Collections'
}
</script>

<style lang="scss" scoped>
.container-fluid{
    margin: 70px 0 ;
    padding: 0;
}

a{
    color: inherit;
}

a:hover {
    color: inherit;
}
.col-4{
    background-size: cover;
    height: 610px;
    position: relative;
    text-align: center;
}

#winter {
    background-image: url('../../assets/images/winter_collection_bg.jpg');
}
#spring{
    background-image: url('../../assets/images/spring_collection_bg.jpg');
}
#autumn{
    background-image: url('../../assets/images/autumn_collection_bg.jpg');
}
h3{
    font-weight: 600;
}
.container-txt{
    position: absolute;
    left: 50%;
    top:70%;
    transform: translate(-50%,-50%);
    color: white;
}

.desc{
    margin: 7px 0 12px 0;
    text-transform: uppercase;
    font-weight: 500;
}

.rounded-pill{
    display: inline-block;
    border: 2px solid white;
    padding: 5px 20px;
    background-color: rgba(255,255,255,0.2);
}

.rounded-pill:hover {
    background-color: rgba(255,255,255,0.3);

}
</style>