<template>
  <header>
    <HeaderTop/>
    <hr>
    <NavBar :links="links"/>
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
            current: false,
            chevron: true

          },
          {
            testo: "Shop",
            current: false,
            chevron: true

          },
          {
            testo: "Products",
            current: false,
            chevron: true

          },
          {
            testo: "Categories",
            current: false,
            chevron: true

          },
          {
            testo: "News",
            current: false,
            chevron: false

          },
          {
            testo: "Elements",
            current: false,
            chevron: true

          }
        ]
      }
    }


}
</script>

<style lang="scss" scoped>

hr{
  width: 100vw;
  color: black;
  margin: 0;
}
</style>