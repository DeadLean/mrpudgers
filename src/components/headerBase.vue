<template>
  <div class="container">
    <div class="header">
      <img src="../assets/img/logo.png" alt="Logo">
      <div class="buttons">
        <button class="logIn" @click="showModal"><img src="../assets/img/headerImg/logIn.svg" alt="logIn" class="logIn_img">Войти</button>
        <button class="reg" @click="showModalReg">Зарегистрироваться</button>
      </div>
      <modal-log-in ref="modal"/>
      <modal-reg ref="modalReg" />
    </div>
  </div>
</template>

<script>
import modalReg from "@/components/modalReg";
import modalLogIn from "@/components/modalLogIn";
export default {
  name: "headerBase",
  components: {
    modalLogIn,
    modalReg
  },
  methods: {
      showModal: function (){
        this.$refs.modal.show = true
      },
    showModalReg: function (){
        this.$refs.modalReg.regShow = true;
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
  .reg{
    width: 200px;
    height: 40px;
    border: #1890FF 1px solid;
    background: none;
    border-radius: 10px;
    margin-left: 20px;
    color: #1890FF;
    font-size: 16px;
  }
</style>