<template>
  <div class="container">
    <div class="header_img">
      <div class="header_text">
        <h1>Онлайн-сервис <br> доставки еды на дом</h1>
        <p>Блюда из любимого ресторана доступны <br> даже у вас дома</p>
      </div>
      <img src="../assets/img/headerImg/header_food.png" alt="food" class="header_food">
    </div>

  </div>
</template>

<script>
export default {
  name: "headerImg"
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
.header_img{
  border-radius: 10px;
  margin-top: 40px;
  width: 100%;
  height: 300px;
  background-color: #1890FF;
  display: flex;
  justify-content: space-between;
}
.header_text{
  margin-left: 70px;
  margin-top: 50px;
}
.header_food{
  width: 450px;
  height: 300px;
}
</style>