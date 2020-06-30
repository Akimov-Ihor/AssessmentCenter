<template>
  <div class="mainPageWrapper">
    <div class="mainPageHeader">
      <div class="mainPageInformation" >
        <span>My Name</span>
        <span>My Surname</span>
        <span>My age</span>
        <span>My job</span>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  
};
</script>

<style scoped>
.mainPageWrapper{
  width: 50vw;
  height: 90vh;
  background-color:whitesmoke ;
}
.mainPageHeader{
  height: 15%;
  background-color: rebeccapurple;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.mainPageInformation{
   width: 75%;
   height: 75%;
   display: flex;
   align-items: center;
   justify-content: space-between;
}


</style>