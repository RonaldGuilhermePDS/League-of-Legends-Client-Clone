<template>
  <div class="sidebarContainer">
    <div class="imageContainer">
      <img class="logo" src="../assets/logo.png" alt="Logo" />
    </div>
    <div class="inputContainer">
      <div class="inputText">
        <p>SignIn</p>
      </div>
      <input placeholder="Username" />
      <input type="password" v-model="characters" placeholder="Password" />
    </div>
    <div class="socialMedia">
      <div class="facebookContainer">
        <img class="social" src="../assets/facebook.png" alt="Facebook" />
      </div>
      <div class="googleContainer">
        <img class="social" src="../assets/google.png" alt="Google" />
      </div>
      <div class="appleContainer">
        <img class="social" src="../assets/apple.png" alt="Apple" />
      </div>
    </div>
    <div class="checkbox">
      <input type="checkbox" />
      <span>Stay Signed In</span>
    </div>
    <div class="buttonContainer">
      <div class="button">
        <img
          :class="{ redButton: characters.length > 3 }"
          class="arrow"
          src="../assets/arrow.svg"
          alt="Next"
        />
      </div>
      <div class="buttonText">
        <p>CAN'T SIGN IN?</p>
        <p>CREATE ACCOUNT</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  /* eslint-disable */
  name: "Sidebar",
  data() {
    return {
      characters: "",
    };
  },
};
</script>

<style scoped>
  input {
    height: 2.75rem;
    background-color: rgb(240, 240, 240);
    margin: 1rem -0.1rem 0rem 0rem;
    padding: 0.5rem;
    border: none;
    outline: none;
    border-radius: 0.2rem;
    transition: 0.2s;
  }
  input:focus {
    border: 0.1rem solid rgb(59, 59, 59);
    background-color: rgb(255, 255, 255);
  }
  input::placeholder {
    font-size: 0.75rem;
    font-weight: 500;
    color: rgb(180, 180, 180);
  }
  input:hover {
    background-color: rgb(235, 235, 235);
  }
  p {
    font-size: 1.2rem;
    letter-spacing: -1.2px;
  }
  .sidebarContainer {
    padding: 3.10rem 2rem 2rem 3.10rem;
    background-color: rgb(250, 250, 250);
    height: 46.45rem;
  }
  .logo {
    width: 7.5rem;
  }
  .inputText,
  .imageContainer,
  .inputContainer,
  .facebookContainer,
  .googleContainer,
  .appleContainer,
  .button {
    display: flex;
    justify-content: center;
  }
  .imageContainer {
    padding-bottom: 2.5rem;
  }
  .inputContainer {
    flex-direction: column;
  }
  .socialMedia {
    margin-top: 1rem;
    height: 1rem;
    display: flex;
    justify-content: space-between;
  }
  .socialMedia > div {
    width: 5rem;
    height: 2rem;
  }
  .social {
    width: 1rem;
  }
  .facebookContainer,
  .googleContainer,
  .appleContainer {
    align-items: center;
    width: 5rem;
    border-radius: 0.2rem;
    cursor: pointer;
  }
  .facebookContainer {
    background-color: #388df5;
  }
  .facebookContainer:hover {
    background: #388df5;
  }
  .googleContainer {
    background-color: #ffffff;
    border: 1.5px solid rgb(255, 255, 255);
  }
  .googleContainer:hover {
    border: 1.5px solid rgb(255, 255, 255);
    background: rgb(248, 248, 248);
  }
  .appleContainer {
    background-color: #000000;
  }
  .appleContainer:hover {
    background: #111111;
  }
  .checkbox {
    display: flex;
    align-items: center;
    margin-top: 0.25rem;
  }
  span {
    font-size: 0.75rem;
    color: #979595;
    padding: 1rem 0rem 0rem 1rem;
  }
  .buttonContainer {
    padding-top: 10rem;
    width: 100%;
  }
  .arrow {
    border: 0.1rem solid #e6e6e6;
    border-radius: 1rem;
    width: 3.5rem;
    padding: 0.8rem;
    cursor: pointer;
  }
  .redButton {
    background-color: rgb(230, 62, 62);
    border: rgb(230, 62, 62);
    cursor: pointer;
  }
  .button {
    width: 100%;
    padding: 0rem 0rem 3.5rem 0rem;
  }
  .buttonText {
    width: 100%;
    text-align: center;
  }
  .buttonText p {
    font-size: 0.65rem;
    word-spacing: 0.1rem;
    color: #c4c4c4;
    cursor: pointer;
  }
  .buttonText p:hover {
    color: #000000;
  }
</style>
