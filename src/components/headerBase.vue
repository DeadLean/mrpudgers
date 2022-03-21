<template>
  <div class="container">
    <div class="header">
      <img src="../assets/img/logo.png" alt="Logo">
      <button class="logIn" @click="showModal"><img src="../assets/img/headerImg/logIn.svg" alt="logIn" class="logIn_img">Войти</button>
      <modal-log-in ref="modal"/>
    </div>
  </div>
</template>

<script>
import modalLogIn from "@/components/modalLogIn";
export default {
  name: "headerBase",
  components: {
    modalLogIn
  },
  methods: {
      showModal: function (){
        this.$refs.modal.show = true
      }
  }
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
  .header{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .logIn{
    width: 100px;
    height: 40px;
    background-color: #1890FF;
    color: white;
    border: none;
    font-size: 16px;
    border-radius: 10px;
  }

</style>