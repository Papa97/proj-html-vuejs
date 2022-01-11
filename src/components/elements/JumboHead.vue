<template>
  <div class="jumbotron">
      <div class="jumbotron__text">
          <div><h1> Brand New Arrivals </h1></div>
          <div><h3>New collection from New York</h3></div>
          <div class="bottoni d-flex justify-content-around">
              <a href="#"><div>View All</div></a>
              <a href="#"><div>Lookbook</div></a>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:'JumboHead'
}
</script>

<style lang="scss" scoped>
.jumbotron{
    height: 600px;
    background-image: url(../../assets/images/home1_slide_three_bg_2.jpg);
    background-size: cover;
    position: relative;
    &__text {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: #fff;
    }
}

h1{
    font-size: 50px;
}
h3{
    font-size: 30px;
    text-transform: uppercase;
}

a{
    text-decoration: none;
}
.bottoni{
    div {
        background-color: rgba(255,255,255,0.3);
        border-radius: 15px;
        padding: 15px 35px;
        border: 2px solid #fff;
        font-size:20px;
        text-transform: uppercase;
        color: white;
    }
}
</style>