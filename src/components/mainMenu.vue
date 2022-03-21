<template>
  <div class="container">
    <h1>Меню</h1>
    <div class="menu">
      <div class="blocks">
        <div class="block">
          <img src="../assets/img/mainMenuImg/pizza.jpg" alt="pizza">
          <div class="block_content">
            <div class="block_header">
              <h3>Пицца</h3>
              <div><p>30 мин</p></div>
            </div>
            <div class="block_footer">
              <p class="rating"><img src="../assets/img/mainMenuImg/star.png" alt="star">4.5</p>
              <p class="price">от 500₽</p>
            </div>
          </div>
        </div>
        <div class="block">
          <img src="../assets/img/mainMenuImg/sushi_and_rolly.jpg" alt="sushi_and_rolly">
          <div class="block_content">
            <div class="block_header">
              <h3>Суши и роллы</h3>
              <div><p>20 мин</p></div>
            </div>
            <div class="block_footer">
              <p class="rating"><img src="../assets/img/mainMenuImg/star.png" alt="star">4.6</p>
              <p class="price">от 600₽</p>
            </div>
          </div>
        </div>
        <div class="block">
          <img src="../assets/img/mainMenuImg/supy.jpg" alt="supy">
          <div class="block_content">
            <div class="block_header">
              <h3>Супы</h3>
              <div><p>40 мин</p></div>
            </div>
            <div class="block_footer">
              <p class="rating"><img src="../assets/img/mainMenuImg/star.png" alt="star">4.5</p>
              <p class="price">от 300₽</p>
            </div>
          </div>
        </div>
        <div class="block">
          <img src="../assets/img/mainMenuImg/noAlko.jpg" alt="noAlko">
          <div class="block_content">
            <div class="block_header">
              <h3>Безалкогольные напитки</h3>
              <div><p>10 мин</p></div>
            </div>
            <div class="block_footer">
              <p class="rating"><img src="../assets/img/mainMenuImg/star.png" alt="star">4.5</p>
              <p class="price">от 200₽</p>
            </div>
          </div>
        </div>
        <div class="block">
          <img src="../assets/img/mainMenuImg/alkoDrinks.jpg" alt="alkoDrinks">
          <div class="block_content">
            <div class="block_header">
              <h3>Алкогольные напитки</h3>
              <div><p>20 мин</p></div>
            </div>
            <div class="block_footer">
              <p class="rating"><img src="../assets/img/mainMenuImg/star.png" alt="star">4.5</p>
              <p class="price">от 500₽</p>
            </div>
          </div>
        </div>
        <div class="block">
          <img src="../assets/img/mainMenuImg/snacks.jpg" alt="snacks">
          <div class="block_content">
            <div class="block_header">
              <h3>Закуски</h3>
              <div><p>15 мин</p></div>
            </div>
            <div class="block_footer" style="margin-top: 20px;">
              <p class="rating"><img src="../assets/img/mainMenuImg/star.png" alt="star">4.5</p>
              <p class="price">от 500₽</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainMenu"
}
</script>

<style scoped>
.container{
  max-width: 70%;
  margin: auto;
  font-family: "Roboto Light";
  color: #302C34;
  text-shadow: 1px 1px 2px pink;
}
.menu{
  width: 100%;
  display: flex;
  justify-content: center;
}
.blocks{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  min-width: 90%;
}
.block{
  max-width: 250px;
  background-color: #fff;
  border-radius: 10px;
  margin-bottom: 20px;
}
.block>img{
  width: 250px;
  height: 150px;
  border-radius: 10px;
}
.block_content{
  margin-right: 15px;
  margin-left: 15px;
}
.block_header{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.block_header>div{
  background-color: #000;
  color: white;
  height: 28px;
  width: 70px;
  font-size: 14px;
  display: flex;
  align-items: center;
  border-radius: 5px;
  justify-content: center;
}

.block_footer{
  display: flex;
}
.rating{
  color: #FFC107;
}
.price{
  margin-left: 10px;
  color: #8C8C8C;
}
</style>