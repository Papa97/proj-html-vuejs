<template>
  <main>
    <FeaturedProducts :feat="featuredArray"/>
    <Collections/>
    <BestSeller :prods="bestSellerArray"/>
    <AdProd/>
    <NewArrivals :arrivals="newArrivalsArray"/>
    <Quote/>
    <OurBlog :posts="ourBlogArray"/>
  </main>
</template>

<script>
import FeaturedProducts from '../elements/FeaturedProducts.vue';
import Collections from '../elements/Collections.vue';
import BestSeller from '../elements/BestSeller.vue';
import AdProd from '../elements/AdProd.vue';
import NewArrivals from '../elements/NewArrivals.vue';
import Quote from '../elements/Quote.vue';
import OurBlog from '../elements/OurBlog.vue';

export default {
    name: 'Main',
    components: {
      FeaturedProducts,
      Collections,
      BestSeller,
      AdProd,
      NewArrivals,
      Quote,
      OurBlog
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
        ],
        dividerArray : [
          'Featured Products',
          'Best Seller',
          'New Arrivals',
        ],

        bestSellerArray : [
          'spring_printed_dress-231x300.jpg',
          'modern_love_tee-200x260.jpg',
          'black_leather_jacket-231x300.jpg',
          'black_elegant_leather_jacket-231x300.jpg',
          'hipster_black_top-231x300.jpg'
        ],

        newArrivalsArray : [
          'black_elegant_leather_jacket-400x520.jpg',
          'hipster_black_top-400x520.jpg',
          'black_leather_suit-400x520.jpg',
          'spring_printed_dress-400x520.jpg',
          'modern_love_tee-400x520.jpg'
        ],

        ourBlogArray : [
          {
            'img' : 'post_img_12-320x202.jpg',
            'titolo' : 'Aenean lobortis sapien enim viverra',
            'data' : 'September 9th, 2015 | 0 comments',
            'sottoTitolo' : 'Donec finibus sit amet orci ebget iltricies. Praesent posuere ante ut erat frigilla.'
          },
          {
            'img' : 'post_img_11-320x202.jpg',
            'titolo' : 'Duic ac massa semper maximus',
            'data' : 'September 9th, 2015 | 0 comments',
            'sottoTitolo' : 'Donec finibus sit amet orci ebget iltricies. Praesent posuere ante ut erat frigilla.'
          },
          {
            'img' : 'post_img_10-320x202.jpg',
            'titolo' : 'Nunc fermint nulla eu justo sem id',
            'data' : 'September 9th, 2015 | 0 comments',
            'sottoTitolo' : 'Donec finibus sit amet orci ebget iltricies. Praesent posuere ante ut erat frigilla.'
          }
        ]
      }
    }    
}
</script>

<style>

</style>