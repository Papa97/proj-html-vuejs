<template>
  <div id="bg-quote">
      <div class="container text-center">
        <div class="image-quote">
            <img src="../../assets/images/man_testimonial.png" alt="">
         </div>
        <div class="txt">
            Curabitur non tristique tortor. Vestibulum aliquet suscipit ipsum in volupat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibhsadip hendrerit bibedum.
        </div>
        <div class="author">Dario Pineda, Theme Fusion</div>
        <div><i class="fas fa-circle punti"></i> <i class="far fa-circle punti"></i></div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Quote'
}
</script>

<style lang="scss" scoped>
#bg-quote{
    background-image: url('../../assets/images/testimonials_home_1_bg.jpg');
    height: 500px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}
.container {
    color: #fff;
    height: 100%;
    .image-quote{
        margin: 20px 0;
        img {
            margin-top:90px;
        }
    }
    .txt{
        width: 75%;
        margin: auto;
        margin-top:30px;
        font-style: italic;
        font-weight: 300;
        font-size: 19px;
    }
    .author{
        margin:30px 0
    }
    .punti {
        font-size: 12px;
    }
}
</style>