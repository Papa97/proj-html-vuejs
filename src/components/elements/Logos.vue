<template>
<div class="sfondo">
  <div class="container text-center">
      <div class="title">brand logos</div>
      <div class="d-flex justify-content-between">
          <div v-for="(logo, index) in list" :key='index'>
              <img :src="require('../../assets/images/' + logo)" alt="">
          </div>
      </div>
    
  </div>
  </div>
</template>

<script>
export default {
    name: 'Logos',
    props : {
       list : Array
    }
}
</script>

<style lang='scss' scoped>


.title{
    text-transform: uppercase;
    font-weight: 600;
    color: #a0a5a5 ;
}

.sfondo {
    background-color : #f1f1f1;
    height: 250px;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>