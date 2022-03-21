<template>
  <div class="footer">
    <div class="container">
      <div class="container_left">
        <img src="../assets/img/logo.png" alt="">
        <div class="links">
          <a href="#">Курьерам</a>
          <a href="#">Пресс-центр</a>
          <a href="#">Контакты</a>
        </div>
      </div>
      <div class="logos">
        <a href="#"><img src="../assets/img/footerImg/inst.png" alt="inst"></a>
        <a href="#"><img src="../assets/img/footerImg/fb.png" alt="fb"></a>
        <a href="#"><img src="../assets/img/footerImg/vk.png" alt="vk"></a>
      </div>
  </div>
  </div>
</template>

<script>
export default {
  name: "siteFooter"
}
</script>

<style scoped>
.footer{
  background-color: #fff;
}
.container{
  padding-top: 10px;
  max-width: 70%;
  margin: auto;
  font-family: "Roboto Light";
  color: #302C34;
  text-shadow: 1px 1px 2px pink;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.container_left{
  display: flex;
  align-items: center;
}
.links{
  display: flex;
  margin-left: 20px;
}
.links>a{
  margin-right: 15px;
  text-decoration: none;
  color: #595959;
}
.logos>a{
  margin-right: 10px;
}
</style>