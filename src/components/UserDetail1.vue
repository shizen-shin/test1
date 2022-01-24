<template>
  <div id="user-detail">
    <h1>ユーザーの詳細ページです</h1>
    <ul class="profile-list">
      <li>ユーザーの名前：{{ name }}</li>
      <li>ユーザーの年齢：{{ age }}</li>
    </ul>
    <p></p>
  </div>
</template>

<script>
export default {
   data(){
     return {
       name: 'Steve',
       age: 24
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
    padding-left: 200px; 
    text-align: left;
    margin: 0 auto;
  }
</style>