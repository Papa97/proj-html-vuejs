<template>
  <div class="container">
      <div class="row">
      <div class="section col-3" id="featured">
          <div class="title">Featured</div>
          <div class="cont-sugg d-flex justify-content-between" v-for="(feat, index) in featured" :key="index">
              <div>
                <span class="nome-prod"> {{feat.nome}}  </span>
                    <div v-if='feat.voto == true' class="voto">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <span v-if="feat.prezzoVecchio" class="prezzo-vecchio">{{feat.prezzoVecchio}} </span>
                    <span class="prezzo" :class="{underline : feat.prezzoVecchio}">
                        {{feat.prezzo}}
                    </span>
              </div>
              
              <div class="immagine-prod">
                  <img :src="require('../../assets/images/' + feat.img)" alt="#">
              </div>
          </div>
      </div>

      <div class="section col-3" id="sale">
          <div class="title">On Sale</div>
          <div class="cont-sugg d-flex justify-content-between" v-for="(sale, index) in onSale" :key="index">
              <div>
                <span class="nome-prod"> {{sale.nome}}  </span>
                    <div v-if='sale.voto == true' class="voto">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <span v-if="sale.prezzoVecchio" class="prezzo-vecchio">{{sale.prezzoVecchio}} </span>
                    <span class="prezzo" :class="{underline : sale.prezzoVecchio}">
                        {{sale.prezzo}}
                    </span>
              </div>
              
              <div class="immagine-prod">
                  <img :src="require('../../assets/images/' + sale.img)" alt="#">
              </div>
          </div>
      </div>

      

      <div class="section col-3" id="top-rated">
          <div class="title">Top Rated</div>
          <div class="cont-sugg d-flex justify-content-between" v-for="(rate, index) in topRated" :key="index">
              <div>
                <span class="nome-prod"> {{rate.nome}}  </span>
                    <div v-if='rate.voto == true' class="voto">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <span v-if="rate.prezzoVecchio" class="prezzo-vecchio">{{rate.prezzoVecchio}} </span>
                    <span class="prezzo" :class="{underline : rate.prezzoVecchio}">
                        {{rate.prezzo}}
                    </span>
              </div>
              
              <div class="immagine-prod">
                  <img :src="require('../../assets/images/' + rate.img)" alt="#">
              </div>
          </div>
      </div>

      <div class="section col-3" id="review">
          <div class="title">Latest review</div>
          <div class="cont-sugg d-flex justify-content-between" v-for="(review, index) in reviews" :key="index">
              <div>
                <span class="nome-prod"> {{review.nome}}  </span>
                    <div v-if='review.voto == true' class="voto">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                <span>by {{review.scritto}}</span>
              </div>
              
              <div class="immagine-prod">
                  <img :src="require('../../assets/images/' + review.img)" alt="#">
              </div>
          </div>
      </div>
      
      
      
      </div>
  </div>
</template>

<script>
export default {
    name: 'Suggestions',
    props: {
        featured : Array,
        onSale : Array,
        topRated : Array,
        reviews : Array
    }
}
</script>

<style lang="scss" scoped>
// #featured {
//     margin-right: 10px;
// }
// #top,
// #sale{
//     margin: 0 10px;
// }
// #latest {
//     margin-left: 10px;
// }
.immagine-prod{
    width: 40%;
    text-align: right;
    img {
        width: 90%;
    }
    
}
.nome-prod{
    font-size: 14px;
}
.cont-sugg {
    margin-bottom: 15px;
    padding-bottom: 15px;
    border-bottom: 1px solid;
    border-color: #a0a5a5;
}
.title{
    text-transform: uppercase;
    margin-bottom: 25px;
}
.voto{
    color: #427ed5;
}
.prezzo {
    font-weight: 500;
}

.prezzo-vecchio {
    font-weight: 500;
    text-decoration: line-through;
}

.underline{
    text-decoration: underline;
}
</style>