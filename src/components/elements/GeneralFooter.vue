<template>
  <div class="sfondo">
      <div class="container">
          <div class="row">
              <div class="col-3">

                  <div>
                      <img src="../../assets/images/classic_shop_logo_footer.png" alt="" class="immagine-footer">
                  </div>
                  <div class="informazioni">
                    <div>12345 North Main Street,</div>
                    <div>New York, NY 555555</div>
                    <div>Phone: 1.800.555.6789</div>
                    <div>Email: info@company.com</div>
                    <div>Web: Theme-fusion.com</div>
                  </div>

                  <div class="loghi">
                    <ul class="general-menu-social">
                        <li class="header-top__fonts">
                            <i class="fab fa-facebook-f"></i>
                        </li>
                        <li class="header-top__fonts"><i class="fab fa-twitter">
                            </i>
                        </li>
                        <li class="header-top__fonts"><i class="fab fa-instagram">
                            </i></li>
                        <li class="header-top__fonts"><i class="fab fa-youtube">
                            </i>
                        </li>
                    </ul>
                  </div>
              </div>
              <div class="col-3">
                  <div class="title">Top Rated Products</div>
                  <div class="d-flex">
                        <div class="colonna">
                            <div class="name">Leather Gloves</div>
                            <div>
                                <div class="voto">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                            </div>
                            <div class="prezzo">$45</div>
                        </div>
                        <div class="colonna text-end"><img src="../../assets/images/leather_gloves-120x156.jpg" alt=""></div>
                  </div>

                  <div class="d-flex">
                        <div class="colonna">
                            <div class="name">Black Leather Jacket</div>
                            <div>
                                <div class="voto">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                            </div>
                            <div class="prezzo">
                                <span class="sbarrato">$235</span>
                                
                                <span class="sottolineato">$200</span> 
                            </div>
                        </div>
                        <div class="colonna text-end"><img src="../../assets/images/black_elegant_leather_jacket-120x156.jpg" alt=""></div>
                  </div>

                  <div class="d-flex">
                        <div class="colonna">
                            <div class="name">Spring Printed Dress</div>
                            <div>
                                <div class="voto">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                            </div>
                            <div class="prezzo">$47</div>
                        </div>
                        <div class="colonna text-end"><img src="../../assets/images/spring_printed_dress-120x156.jpg" alt=""></div>
                  </div>
                  
              </div>
              <div class="col-3">
                  <div class="title">Recent Posts</div>
                  <div >
                      <div v-for="(post, index) in posts" :key="index" class="posts">
                        <i class="fas fa-chevron-right"></i>  <span> {{post}} </span>
                      </div>
                  </div>
              </div>
              <div class="col-3">
                  <div class="title">Tags</div>
                  <div class="cont-tags">
                      <div v-for="(tag, index) in tags" :key="index"> 
                       {{tag}}   
                      </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:'GeneralFooter',
    props : {
        posts:Array,
        tags: Array
    }

}
</script>

<style lang='scss' scoped>
.col-3 {
    margin-top: 75px ;
    margin-bottom: 80px;
}
.immagine-footer{
    width: 70%;
}
.sfondo {
    background-color: #2b2e32;
    color: white;
}

.informazioni{
    margin-top: 30px;
    margin-bottom: 30px;
}
.general-menu-social {
    display: flex;
    list-style: none;
    margin: 0;
    padding-left: 0;
    li{
        padding:0 5px
    }
    .last-li{
        border-right: none;
        padding: 0 40px;
        text-transform: uppercase;
        span {
            margin: 0 10px;
        }
    }
}

.d-flex{
    margin-top: 20px;
    border-bottom: 1px solid #40474d;
    padding-bottom: 10px;
    img {
        height: 75px
    }
}

.name{
    font-size: 14px;
}

.colonna {
    width:50%
}

.voto{
    color: #427ed5;
}

.prezzo {
    font-weight: 600;
}

.sbarrato {
    text-decoration: line-through;
}

.sottolineato {
    text-decoration: underline;
    margin-left: 4px;
}

.title {
    text-transform: uppercase;
    font-weight: 600;
    margin-bottom:20px;
}

.posts {
    font-weight: 400;
    line-height: 1.6;
    padding: 10px 0;
    border-bottom: 1px solid #40474d;
}

.cont-tags {
    display: flex;
    flex-wrap:wrap;
    font-weight: 500;
    div {
        padding: 2px 5px;
        margin: 2px;
        border: 1px solid #40474d;
    }
}
</style>