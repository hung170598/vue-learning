<template>
  <div id="Header">
    <nav class="header">
      <img class="logo" src="../assets/img/logo.c5be62e9.png" />
      <ul class="menu">
        <li><a href="/">Trang Chủ</a></li>
        <li><a href="/lesson">Bài Giảng</a></li>
        <li><a href="/video">Video Bài Giảng</a></li>
        <li><a href="/quizz">Bài Tập</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
  list-style: none;
}
.header {
  background: white;
  height: 60px;
  width: 100%;
  line-height: 60px;
  display: flex;
  position: fixed;
}
.logo {
  margin-left: 15px;
}
.menu {
  display: flex;
  margin-left: 15px;
}
.menu li a {
  color: black;
  font-weight: bold;
  padding: 0px 30px;
  display: inline-block;
}
.menu li a:hover {
  color: white;
  background-color: red;
}
</style>