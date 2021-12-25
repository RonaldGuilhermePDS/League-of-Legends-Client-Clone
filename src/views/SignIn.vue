<template>
  <div class="container">
    <Sidebar />
  </div>
</template>

<script>
  import Sidebar from "../components/Sidebar";
  export default {
    name: "App",
    components: {
      Sidebar,
    },
  };
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@600;900&display=swap");
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    text-decoration: none;
    font-family: "Poppins", sans-serif;
  }
  .container {
    background: linear-gradient(rgba(61, 82, 81, 0.138), rgba(61, 82, 81, 0.138)),
    url("../assets/Login_image.jpg");
    background-size: cover;
    background-attachment: fixed;
    background-position: center;
    padding-right: 75%;
  }
</style>
