<template>
  <div class="mainPageWrapper">
    <div class="mainPageWrapperCenter"></div>
  </div>
</template>



<script>
// import axios from "axios";

export default {
  //   data() {
  //     return {
  //       login: "",
  //       password: "",
  //       token:'',
  //       auth:false
  //     };
  //   },
  //   methods: {
  //     async onSubmit() {
  //     const response =  await axios
  //          .post(
  //           "http://ec2-3-22-241-132.us-east-2.compute.amazonaws.com/api/token/",
  //           { sAMAccountName: this.login, password: this.password }
  //         )
  //       this.password = "";
  //       this.login = "";
  //           this.token=response.data.access
  //           console.log(this.token)
  //        await axios
  //           .get(
  //           "http://ec2-3-22-241-132.us-east-2.compute.amazonaws.com/user/users",
  //           { headers: { 'Authorization': `Bearer ${this.token}` } })
  //         .then(response=>{
  //           if(response.status==200){
  //           this.auth=!this.auth
  //           }
  //         })
  //         .catch(e => {
  //           console.log("gg", e);
  //         });
  //         console.log(this.auth)
  //     }
};
</script>

<style scoped>
.mainPageWrapper {
  background-color: whitesmoke;
  /* background: url("../assets/background .jpg") no-repeat center;
  background-size: cover; */
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

.mainPageWrapper::before {
  content: "";
  display: block;
  position: absolute;
  z-index: -1;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  /* background-color: rgba(255,255,255,0.9); */
  /* background-color: rgba(78, 140, 134, 0.83); */
  filter: blur(0.5px);
}
.mainPageWrapperCenter {
  background: aquamarine;
  width: 27vw;
  height: 65vh;
  display: flex;
  font-family: "Trebuchet MS";
}
