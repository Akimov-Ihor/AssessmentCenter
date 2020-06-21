<template>
  <div class="loginWrapper">
    <div class="loginWrapperCenter">
      <div class="signIn">
        <h1>Sign In</h1>
        <div class="signInBySocialMedia">
          <img src="../assets/login.jpg" />
        </div>
        <span class="adviceLoginPage">Ensure your email for registration</span>

        <div class="form">
          <input type="text" name="name" autocomplete="off" placeholder=" " />
          <label for="name" class="label-name">
            <span class="content-name">Email</span>
          </label>
        </div>
        <div class="form">
          <input type="password" name="password" autocomplete="off" placeholder=" " />
          <label for="password" class="label-name">
            <span class="content-name">Password</span>
          </label>
        </div>

        <a href="#">Forgot your password?</a>
        <button>Sign In</button>
      </div>
      <!-- <div class="signUp">
        <h2>Hello Friend</h2>
        <p>Enter your personal details and start journey with us</p>
        <button>Sign up</button>
      </div>-->
    </div>
  </div>
</template>



<script>
export default {
  components: {}
};
</script>

<style scoped>
.loginWrapper {
  /* background-color: whitesmoke; */
  background: url("../assets/background .jpg") no-repeat center;
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

.loginWrapper::before {
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
.loginWrapperCenter {
  background: aquamarine;
  width: 27vw;
  height: 65vh;
  display: flex;
  font-family: "Trebuchet MS";
}
.signIn {
  position: relative;
  margin: 0;
  padding: 0;
  background: white;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: left;
}
.signInBySocialMedia {
  width: 35%;
  height: 29%;
  display: flex;
  justify-content: space-between;
}
.signInBySocialMedia > img {
  width: 100%;
  height: 100%;
}
h1 {
  margin: 0;
  padding: 3rem;
  font-size: 3rem;
}
.login {
  display: flex;
  flex-direction: column;
  width: 100%;
  /* align-items: center; */
}

/* Input */
.form {
  width: 75%;
  position: relative;
  height: 8%;
  overflow: hidden;
}
.form input {
  width: 100%;
  height: 100%;
  color: black;
  padding-top: 2%;
  border: none;
  outline: 0;
  font-size: 20px;
  /* margin-block: 0; */
}
.form label {
  position: absolute;
  bottom: 0px;
  left: 0%;
  width: 100%;
  height: 100%;
  pointer-events: none;
  border-bottom: 1px solid black;

  /* background: blue; */
}
.form label::after {
  content: "";
  position: absolute;
  height: 100%;
  width: 100%;
  border-bottom: 3px solid rgb(0, 9, 139);
  left: 0px;
  bottom: -4px;
  transform: translateX(-100%);
  transition: transform 0.3s ease;
}
.content-name {
  position: absolute;
  bottom: 5px;
  left: 0px;
  transition: all 0.6s ease;
}
.form input:focus + .label-name .content-name {
  transform: translateY(-120%) scale(0.8);
  font-size: 14px;
  color: rgb(48, 172, 130);
  font-weight: bold;
}
.form input:not(:placeholder-shown) + .label-name .content-name {
  transform: translateY(-120%) scale(0.8);
  font-size: 15px;
  color: rgb(48, 172, 130);
  font-weight: bold;
}
.form input:focus + .label-name::after,
.form input:label + .label-name ::after {
  transform: translateX(0%);
}

/* Input END */
.adviceLoginPage {
  font-weight: bolder;
}

a {
  text-decoration: none;
  color: #2c3e50;
  margin-bottom: 4%;
  margin-top: 4%;
}
a:hover {
  color: #129287;
}
button {
  text-decoration: none;
  outline: none;
  display: inline-block;
  padding: 10px 30px;
  margin: 10px 20px;
  position: relative;
  overflow: hidden;
  border: 1px solid black;
  border-radius: 8px;
  font-family: "Montserrat", sans-serif;
  color: #2c3e50;
  transition: 0.2s ease-in-out;
}
button:before {
  content: "";
  background: linear-gradient(
    90deg,
    rgba(255, 255, 255, 0.1),
    rgba(255, 255, 255, 0.5)
  );
  height: 50px;
  width: 50px;
  position: absolute;
  top: -8px;
  left: -75px;
  transform: skewX(-45deg);
}
button:hover {
  background: #129287;
  color: white;
}
button:hover:before {
  left: 150px;
  transition: 0.5s ease-in-out;
}

@media (min-width: 1200px) {
  .loginWrapperCenter[data-v-5faf54d0] {
    background: aquamarine;
    width: 27vw;
    height: 70vh;
    display: flex;
    font-family: "Trebuchet MS";
  }
  h1 {
    margin: 0;
    padding: 2rem;
    font-size: 2rem;
  }
}

/* Landscape tablets and medium desktops */
@media (min-width: 992px) and (max-width: 1199px) {
  .loginWrapperCenter {
    background: aquamarine;
    width: 39vw;
    height: 100vh;
    display: flex;
    font-family: "Trebuchet MS";
  }
  .form input {
    font-size: 15px;
    padding-top: 0%;
  }
}

/* Portrait tablets and small desktops */
@media (min-width: 768px) and (max-width: 991px) {
  h1 {
    margin: 0;
    padding: 0;
    font-size: 2rem;
  }
  .loginWrapperCenter {
    width: 39vw;
    height: 74vh;
  }
}

/* Landscape phones and portrait tablets */
@media (max-width: 767px) {
  .loginWrapperCenter {
    width: 59vw;
    height: 69vh;
   
  }
}

/* Portrait phones and smaller */
@media (max-width: 480px) {
  .loginWrapperCenter {
    width: 97vw;
    height: 59vh;
  }
}

/* Iphone 5 */
@media (max-width: 320px) {
  .loginWrapperCenter {
    width: 99vw;
    height: 102vh;
   
  }
}

@media (max-height: 480px) {
  .loginWrapperCenter {
    background: aquamarine;
    width: 63vw;
    height: 96vh;
    
  }
  h1 {
    margin: 0;
    padding: 0;
    font-size: 2rem;
  }
}
</style>