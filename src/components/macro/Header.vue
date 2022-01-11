<template>
  <header>
    <HeaderTop/>
    <hr>
    <NavBar/>
    <JumboHead/>
  </header>
</template>

<script>
import NavBar from '../elements/NavBar.vue';
import JumboHead from '../elements/JumboHead.vue';
import HeaderTop from '../elements/HeaderTop.vue';

export default {
    name: 'Header',
    components: {
      NavBar,
      JumboHead,
      HeaderTop
    },
    data() {
      return {
        links: [
          {
            testo: "Home",
            currnet: "false",
          },
          {
            testo: "Shop",
            currnet: "false",
          },
          {
            testo: "Products",
            currnet: "false",
          },
          {
            testo: "Categories",
            currnet: "false",
          },
          {
            testo: "News",
            currnet: "false",
          },
          {
            testo: "Elements",
            currnet: "false",
          }
        ]
      }
    }


}
</script>

<style lang="scss" scoped>

hr{
  margin: 0;
  width: 100vw;
  color: #ababab;
}
</style>