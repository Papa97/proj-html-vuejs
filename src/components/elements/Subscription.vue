<template>
  <div class="sfondo d-flex align-items-center">
      <div class="container text-center">
        <div class="icon rounded-circle"> <i class="far fa-envelope"></i> </div>
        <span class="text">Subscribe now and get special offers </span>
        <input class="rounded-pill" type="text" placeholder='Insert your email'>
        <button class="rounded-pill">Send</button>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Subscription',
}
</script>

<style lang='scss' scoped>
.sfondo {
    background-color: #2f3034;
    height: 175px;
}
.container{
    color: white
}
input{
    border: 0;
    padding: 5px 40px;
    color: #a0a5a5;
    margin: 0 10px;
}

button {
    background-color: #427ed5;
    color: white;
    text-transform: uppercase;
    font-weight: 600;
    padding: 5px 40px;
    border: 0;
}

.text {
    font-weight: 700;
    margin-left: 15px;
}

.icon {
    display: inline;
    background-color: #292a2e;
    padding: 15px 14px 11px;
    svg {
        font-size : 22px;
    }
}


</style>