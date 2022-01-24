<template>
  <div id="user-detail">
    <h1>ユーザーの詳細ページです</h1>
    <ul class="profile-list">
      <li>苗字：<input type="text" v-model="lastName" ></li>
      <li>名前：<input type="text" v-model="firstName" ></li>
      <li>フルネーム：{{ fullName }}</li>
    </ul>
    <p></p>
  </div>
</template>

<script>
export default {
  data(){
    return{
      lastName: '',
      firstName: '',
      fullName: '',
    }
  },
  watch:{
    lastName: function(){
      this.fullName = this.lastName + " " + this.firstName
    },
    firstName: function(){
      this.fullName = this.firstName + " " + this.lastName
    }
  }
}
</script>

<style scoped>
  #user-detail{
    margin: 0 auto;
    width: 800px;
    border: 10px solid red;
  }
  .profile-list{
    margin: 40px auto;
    padding-left: 200px; 
    text-align: left;
  }
</style>