<template>
  <div id="app">
    <header-base />
    <header-img />
    <main-menu />
    <site-footer />

  </div>
</template>

<script>
import headerBase from './components/headerBase.vue';
import headerImg from "@/components/headerImg";
import mainMenu from "@/components/mainMenu";
import siteFooter from "@/components/siteFooter";


export default {
  name: 'App',
  components: {
    headerBase,
    headerImg,
    mainMenu,
    siteFooter,

  },
  methods: {
    showModal: function () {
      this.$refs.modal.show = true
    }
  }
}
</script>

<style>
#app{
  margin: 0;
  background-color: #F5F5F5;
}
</style>
