<template>
  <main>
    <FeaturedProducts :feat="featuredArray"/>
    <Collections/>
    <BestSeller :prods="bestSellerArray"/>
    <AdProd/>
    <NewArrivals :arrivals="newArrivalsArray"/>
    <Quote/>
    <OurBlog :posts="ourBlogArray"/>
    <Suggestions :featured="featuredArrayBottom" :onSale="sales" :topRated="topRated" :reviews='latestReview'/>
    <Logos :list="logoBottom"/>
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
import Suggestions from '../elements/Suggestions.vue';
import Logos from '../elements/Logos.vue';

export default {
    name: 'Main',
    components: {
      FeaturedProducts,
      Collections,
      BestSeller,
      AdProd,
      NewArrivals,
      Quote,
      OurBlog,
      Suggestions,
      Logos
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
          {
            'img' : 'spring_printed_dress-231x300.jpg',
            'title' : 'Spring Printed Dress',
            'desc' : 'Woman, Dress',
            'prize' : '$47'
          },
          {
            'img' : 'modern_love_tee-200x260.jpg',
            'title' : 'Spring Printed Dress',
            'desc' : 'Woman, Dress',
            'prize' : '$69'
          },
          {
            'img' : 'black_leather_jacket-231x300.jpg',
            'title' : 'Black Jacket',
            'desc' : 'Woman, Jacket, Jeans',
            'prize' : '$200'
          },
          {
            'img' : 'black_elegant_leather_jacket-231x300.jpg',
            'title' : 'Black Elengant Jacket',
            'desc' : 'Men, Jacket, elegant',
            'prize' : '$200'
          },
          {
            'img' : 'hipster_black_top-231x300.jpg',
            'title' : 'Hipster Black Top',
            'desc' : 'Woman, Top',
            'prize' : '$200'
          }
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
        ],
        featuredArrayBottom : [
          {
            'nome' : 'Black Jacket',
            'voto' : false,
            'prezzo' : '$125',
            'img' : 'black_leather_jacket-120x156.jpg'
          },
          {
            'nome' : 'Black Leather Jacket',
            'voto' : true,
            'prezzo' : '$200',
            'prezzoVecchio' : '$235',
            'img' : 'black_elegant_leather_jacket-120x156.jpg'

          },
          {
            'nome' : 'Hipster Black Top',
            'voto' : false,
            'prezzo' : '$57',
            'img' : 'hipster_black_top-120x156.jpg'
          }
        ],
        sales : [
            {
            'nome' : 'Black Leather Jacket',
            'voto' : true,
            'prezzo' : '$200',
            'prezzoVecchio' : '$235',
            'img' : 'black_elegant_leather_jacket-120x156.jpg'
            },
            {
            'nome' : 'Blue Leather Jacket',
            'voto' : false,
            'prezzo' : '$60',
            'prezzoVecchio' : '$80',
            'img' : 'blue_leather_jacket-120x156.jpg'
            },
            {
            'nome' : 'Modern Leather Boots',
            'voto' : false,
            'prezzo' : '$30',
            'prezzoVecchio' : '$50',
            'img' : 'modern_leather_boots-120x156.jpg'
            }
            
        ],
        topRated : [
            {
            'nome' : 'Leather Gloves',
            'voto' : true,
            'prezzo' : '$45',
            'img' : 'leather_gloves-120x156.jpg'
            },
            {
            'nome' : 'Black Leather Jacket',
            'voto' : true,
            'prezzo' : '$200',
            'prezzoVecchio' : '$235',
            'img' : 'black_elegant_leather_jacket-120x156.jpg'
            },
            {
            'nome' : 'Spring Printed dress',
            'voto' : true,
            'prezzo' : '$47',
            'img' : 'spring_printed_dress-120x156.jpg'
            }
        ],
        latestReview : [
          {
            'nome' : 'Black Leather Jacket',
            'voto' : true,
            'img' : 'black_elegant_leather_jacket-120x156.jpg',
            'scritto' : 'admin'
            },
            {
            'nome' : 'Leather Gloves',
            'voto' : true,
            'img' : 'leather_gloves-120x156.jpg',
            'scritto' : 'BeardMan'

            },
            {
            'nome' : 'Spring Printed dress',
            'voto' : true,
            'img' : 'spring_printed_dress-120x156.jpg',
            'scritto' : 'admin'
            }
        ],
        logoBottom : [
          'b_logotype_6.png',
          'b_logotype_7.png',
          'b_logotype_1.png',
          'b_logotype_2.png',
          'b_logotype_3.png'
        ]
      }
    }    
}
</script>

<style>

</style>