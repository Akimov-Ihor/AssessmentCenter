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
          <input type="text" name="password" autocomplete="off" placeholder=" " />
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
      </div> -->
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
  background-color: whitesmoke;
  height: 100vh;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
.loginWrapperCenter {
  background: aquamarine;
  width: 41vw;
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
.signInBySocialMedia>img {
  width: 100%;
  height: 100%;
}
h1 {
  margin: 0;
  padding: 3rem;
  font-size: 3rem;
}
.signUp {
  margin: 0;
  padding: 0;
  /* background: white; */
  width: 35%;
  color: white;
  height: 100%;
  display: flex;
  flex-direction: column;
  /* justify-content: center; */
  align-items: center;
}
.signUp > p {
  font-size: 1rem;
  padding: 0 1rem;
  font-weight: bold;
}

h2 {
  margin: 0;
  padding: 4rem 2rem 1rem 2rem;
  font-size: 2rem;
  font-weight: bold;
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
</style>