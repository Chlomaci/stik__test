<script>

</script>

<template>
  <div id="app">
    <header>
      <div class="menu">
        <div class="menu__variants">
          <img src="@/assets/Search.svg" alt="search" class="menu__search mobile">
          <img src="@/assets/User.svg" alt="user" class="menu__user mobile">
        </div>
        <div class="menu__logo">
          <img src="@/assets/logo.png" alt="logo">
        </div>
        <div class="menu__variants">
          <img src="@/assets/Search.svg" alt="search" class="menu__search desktop">
          <img src="@/assets/Favorite.svg" alt="favorite" class="menu__favorite desktop">
          <img src="@/assets/User.svg" alt="user" class="menu__user desktop">
          <img src="@/assets/Basket.svg" alt="basket" class="menu__basket desktop" id="basket">
        </div>
      </div>
    </header>
    <main>
      <div class="main">
        <div class="main__slides">
          <img src="@/assets/coatFront.png" alt="coat front">
          <img src="@/assets/coatBack.png" alt="coat back">
          <img src="@/assets/coatFocus.png" alt="coat focus">
        </div>
        <div class="main__img">
          <img src="@/assets/mainImg.png" alt="coat">
          <div class="img__points">
            <div class="point active"></div>
            <div class="point"></div>
            <div class="point"></div>
            <div class="point"></div>
          </div>
        </div>
        <div class="main__descr">
          <div class="descr">
            <div class="descr__titles">
              <div class="descr__title">Жакет удлиненный, белый</div>
              <div class="descr__subtitle">8900 RUB</div>
            </div>
            <img src="@/assets/Favorite.svg" alt="add to favorites" class="mobile">
          </div>
          <div class="sizes">
            <div class="sizes__title">Размеры</div>
            <div class="sizes__variants">
              <div class="sizes__variant">XS</div>
              <div class="sizes__variant">S</div>
              <div class="sizes__variant absent">M</div>
              <div class="sizes__variant quantity">мало</div>
              <div class="sizes__variant quantity empty"></div>
              <div class="sizes__variant quantity absent">подписка</div>
            </div>
          </div>
          <div class="colors">
            <div class="colors__title">Цвет: белый</div>
            <div class="colors__variants">
              <div class="color__variant white"></div>
              <div class="color__variant black"></div>
              <div class="color__variant beige"></div>
              <div class="color__variant activeLine"></div>
              <div class="color__variant empty"></div>
              <div class="color__variant empty"></div>
            </div>
          </div>
          <div class="basket">
            <div class="basket__add">Добавить в корзину</div>
            <div class="basket__favorite">
              <img src="@/assets/Favorite.svg" alt="add to favorites">
            </div>
          </div>
          <div class="product">
            <div class="product__item">
              <div class="product__title">Описание</div>
              <img src="@/assets/Plus.svg" alt="show">
            </div>
            <div class="product__item">
              <div class="product__title">Состав и уход</div>
              <img src="@/assets/Plus.svg" alt="show">
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Helvetica', sans-serif;
  font-weight: 200;
}

.menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-left: auto;
  margin-top: 31px;
  margin-bottom: 31px;
  padding-right: 48px;
}

.menu__variants{
  display: flex;
  justify-content: space-between;
  img {
    margin-left: 16px;
    width: 24px;
    height: 24px;
  }
  .mobile{
    display: none;
  }
}
.main{
  display: grid;
  justify-content: center;
  column-gap: 30px;
  grid-template-columns: 15% 30% 30%;
 }

.main__slides{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-end;
  height: 300px;
  row-gap: 10px;
  img {
    width: 100px;
    height: 120px;
  }
}

.main__img{
  width: 100%;
  img {
    width: 100%;
  }
}

.img__points{
  display: none;
}

.main__descr{
  display: grid;
  grid-template-rows: repeat(5, 10%);
  row-gap: 35px;
}

.descr .mobile{
  display: none;
}

.descr__title{
  font-size: 1.5rem;
  text-transform: uppercase;
  color: #333333;
  .descr__subtitle{
    margin-top: 8px;
  }
}

.sizes{
  font-size: 1.2rem;
  color: #4F4F4F;
}
 .sizes__title{
   margin-bottom: 8px;
 }

.sizes__variants {
  display: grid;
  grid-template-columns: repeat(3, 100px);
  grid-template-rows: 40px 10px;
  justify-items: center;
  column-gap: 14px;
}

.sizes__variant{
  text-align: center;
  line-height: 40px;
  width: 100%;
  height: 100%;
  border: 1px solid black;
}
.sizes__variant.quantity {
  border: none;
  color: #828282;
}

.colors{
  font-size: 1.2rem;
  color: #4F4F4F;
}

.colors__variants{
  display: grid;
  grid-template-columns: repeat(3, 50px);
  grid-template-rows: 45px 2px;
  column-gap: 14px;
  row-gap: 3px;
  margin-top: 8px;
}

.color__variant{
  margin-left: 2px;
  margin-right: 2px;;
}

.color__variant.empty{
  margin: 0;
}

.color__variant.activeLine{
  margin: 0;
  background-color: #000000;
}

.color__variant.white {
  border: 1px solid #BDBDBD;
}

.color__variant.black {
  background-color: #000000;
}

.color__variant.beige {
  background-color: #F9F1DC;
}

.basket{
  display: flex;
  max-width: 400px;
  height: 65px;
  justify-content: space-between;
}

.basket__add{
  width: 80%;
  font-size: 1.3rem;
  background-color: black;
  color: white;
  text-align: center;
  vertical-align: middle;
  line-height: 37px;
  padding-top: 15px;
  padding-bottom: 15px;
}

.basket__favorite{
  width: 15%;
  padding: 10px;
  border: 1px solid black;
  display: flex;
  justify-content: center;
  align-content: center;
}

.product{
  height: 70px;
}

.product__item{
  border: 1px solid #E0E0E0;
  border-left: none;
  border-right: none;
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  img{
    height: 30%;
  }
}

.product__title{
  font-size: 1.3rem;
  color: #333333;
  text-align: center;
  vertical-align: middle;
  line-height: 37px;
}

@media (max-width: 1440px){
  .main__descr{
    grid-template-rows: repeat(5, auto);
  }
  .descr__title {
    font-size: 1rem;
  }
  .sizes{
    font-size: 1rem;
  }
  .colors{
    font-size: 1rem;
  }
  .basket__add{
    font-size: 1rem;
  }
  .product__title{
    font-size: 1rem;
  }
}

@media (max-width: 1024px){
   .main {
     padding-right: 172px;
   }
}

@media (max-width: 768px){
  .descr{
  }

  .main__slides{
    height: 150px;
    img {
      width: 50px;
      height: 70px;
    }
  }
}

@media (max-width: 425px){
  .menu__variants .desktop{
    display: none;
  }
  .menu__variants {
    img.mobile{
      display: block;
    }
  }
  #basket{
    display: block;
  }

  .menu{
    max-width: 100%;
    margin-left: 0;
    padding-right: 0;
  }

  .main{
    display: grid;
    justify-content: center;
    padding-left: 172px;
    padding-right: 172px;
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, auto);
    row-gap: 50px;
  }

  .main__slides{
    display: none;
  }
  .main__img{
    width: 100vw;
    padding: 0;
    position: relative;
    img {
      width: 100%;
    }
  }

  .img__points{
    display: flex;
    width: 100%;
    justify-content: center;
    position: absolute;
    bottom: 17px;
  }

  .point{
    width: 10px;
    height: 10px;
    background-color: rgb(255, 255, 255, 0.25);
    border-radius: 50px;
    margin-right: 7px;
    &.active {
      background-color: white;
    }
  }

  .main__descr{
    padding-left: 20px;
    padding-right: 20px;
  }
  .descr__title{
    margin-bottom: 5px;
  }
  .descr{
    display: flex;
    width: 100%;
    justify-content: space-between;
  }

  .descr .mobile{
    display: block;
    height: 100%;
  }
  .sizes{
    color: #4F4F4F;
  }
  .basket {
    display: none;
  }
}
</style>
