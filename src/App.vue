<template>
  <div id="app">
    <LoginPage v-if="this.auth===false" @changeIsAuth="isAuth" />
    <MainPage v-else-if="this.auth===true" />
  </div>
</template>

<script>
debugger
import LoginPage from "./components/LoginPage.vue";
import MainPage from "./components/MainPage.vue";

export default {
  name: "App",
  data() {
    return {
      auth: false
    };
  },
  methods:{
   isAuth:function ChangeMainAuth(){
      return this.auth=!this.auth
   }
  
  },
  components: {
    LoginPage,
    MainPage
  }
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  /* background-color: whitesmoke; */
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  background: url("./assets/background .jpg") no-repeat center;
  background-size: cover;
  opacity: 1;
  position: relative;
  height: 100vh;
  padding: 0;
  z-index: 1;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

#app::before {
  content: "";
  display: block;
  position: absolute;
  z-index: -1;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  /* background-color: rgba(255,255,255,0.9); */
  background-color: rgba(78, 140, 134, 0.83);
  filter: blur(0.5px);
}
</style>
