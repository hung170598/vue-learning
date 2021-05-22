<template>
  <div id="Footer">
    <nav class="footer">
      <h2>Contact Us</h2>
      <ul class="contact">
        <li>
          <a href="https://www.facebook.com" target="_blank">
            <img src="../assets/img/facebook.e4700f80.png" width="50px" />
          </a>
        </li>
        <li>
          <a href="https://mail.google.com/" target="_blank">
            <img src="../assets/img/gmail.9b4b7415.png" width="50px" />
          </a>
        </li>
        <li>
          <a href="https://www.youtube.com" target="_blank">
            <img src="../assets/img/youtube.63d08e28.png" width="68px" />
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
  list-style: none;
}
.footer {
  background-color: #555555;
  text-align: center;
  bottom: 0;
  width: 100%;
  position: fixed;
}
h2 {
  color: white;
}
.contact {
  display: flex;
  justify-content: center;
}
.contact li {
  padding: 0 1em;
}
</style>