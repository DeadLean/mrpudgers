<template>
  <div v-if="show" class="modal-shadow" @click.self="closeModal">
    <div class="modal">
      <div>
        <div class="modal-close" @click="closeModal">&#10006;</div>
        <slot name="title">
          <h2 class="modal_title">Авторизоваться</h2>
        </slot>
        <slot name="body">
          <div class="body">
            <input placeholder="Введите номер телефона" type="tel" class="tel">
            <input type="password" placeholder="Введите пароль" class="password">
            <button>Войти</button>
          </div>
        </slot>
        <slot name="footer" class="footer">
          <h3>У меня нет аккаунта :(</h3>
          <a href="#" class="wantReg">Хочу зарегестрироваться!</a>
        </slot>
      </div>
      </div>
  </div>
</template>

<script>
export default {
  name: "modalLogIn",
  data: function () {
    return{
      show: true
    }
  },
  methods: {
    closeModal: function (){
      this.show = false
    }
  }
}
</script>

<style scoped>
.modal-shadow {
  position: absolute;
  top: 0;
  left: 0;
  min-height: 100%;
  width: 100%;
  background: rgba(0, 0, 0, 0.39);
}

.modal {
  background: #fff;
  border-radius: 8px;
  padding: 15px;
  min-width: 350px;
  max-width: 400px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  justify-content: center;
}
.modal-close{
  display: flex;
  justify-content: end;
}
.modal_title{
  display: flex;
  justify-content: center;
}
.body{
  display: grid;
  grid-template-columns: auto;
  max-width: 200px;
}
input{
  margin-bottom: 10px;
  border-radius: 10px;
  border: 1px #8C8C8C solid;
  height: 30px;
}
button{
  width: 100px;
  height: 25px;
  margin-left: 20%;
  border: none;
  border-radius: 10px;
  background-color: #1890FF;
  color: white;
}
a{
  text-decoration: none;
  color: #1890FF;
}
</style>