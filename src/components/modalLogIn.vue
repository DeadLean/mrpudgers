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
            <input placeholder="Введите номер телефона" type="tel" class="tel" v-model="number">
            <input type="password" placeholder="Введите пароль" class="password" v-model="password">
            <button @click="logIn">Войти</button>
          </div>
        </slot>
      </div>
      </div>
    <modal-reg />
  </div>
</template>

<script>
import modalReg from "@/components/modalReg";
export default {
  name: "modalLogIn",
  components: {
    modalReg
  },

  data: function () {
    return{
      show: false,
      users: [
        {
          id: 0,
          tel: 1,
          pass: 1111,
          admin: 0
        },
        {
          id: 1,
          tel: 2,
          pass: 2222,
          admin: 1
        }
      ],
      number: '',
      password: ''
    }
  },
  methods: {
    closeModal: function (){
      this.show = false
    },
    logIn: function (){
      if (this.number == this.user.tel){
        console.log(1)
      }

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
</style>