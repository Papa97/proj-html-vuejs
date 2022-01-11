<template>
  <main>
    <FeaturedProducts :feat="featuredArray"/>
    <Collections/>
  </main>
</template>

<script>
import FeaturedProducts from '../elements/FeaturedProducts.vue';
import Collections from '../elements/Collections.vue'
export default {
    name: 'Main',
    components: {
      FeaturedProducts,
      Collections
    },
    data() {
      return {
        featuredArray: [
          {
            'img' : 'black_elegant_leather_jacket-400x520.jpg',
            'descrizione' : 'Black Leather Jacket',
            'keyWord' : 'Men, Jackets, Jeans',
            'prezzoListino' : '235',
            'prezzoSconto' : '200'
          },
          {
            'img' : 'black_leather_suit-400x520.jpg',
            'descrizione' : 'Black Leather Suit',
            'keyWord' : 'Men, Jackets',
            'prezzoSconto' : '176'
            
          },
          {
            'img' : 'blue_jacket_and_white_stripe_tee-400x520.jpg',
            'descrizione' : 'Blue Jacket & Stripe Tee',
            'keyWord' : 'Men, Jackets, Suits',
            'prezzoSconto' : '580'

          },
          {
            'img' : 'modern_black_leather_suit-400x520.jpg',
            'descrizione' : 'Modern Black Leather Suit',
            'keyWord' : 'Men, Jackets',
            'prezzoSconto' : '96'

          }
        ]
      }
    }    
}
</script>

<style>

</style>