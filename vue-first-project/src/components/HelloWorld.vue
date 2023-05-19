<template>
  <div class="teste">First-Project-Vue</div>
  <h1 class="umbrella-corporation">New to Umbrella?</h1>
  <a class="create-account" href="https://discord.gg/umbrella">Create account</a>
  <div class="pagina-de-registro"></div>
  <div class="umbrella-corp">
    <img class="umbrella-corp-img" src="https://cdn.discordapp.com/attachments/1050050229946294362/1108890115360690206/1080x1080.png">
  </div>
  <div class="pagina-de-login">
    <input class="username" v-model="inputText">
    <div class="username-text">Username or email address</div>
    <div class="button-confirm">
      <button class="button-confirmed">Sign In</button>
      <button class="forgot-password" href="#">Forgot Password?</button> 
    </div>
    <div class="text-password">Password</div>
    <input class="input-password" v-model="inputPassword" maxlength="25" :type="inputType">
    <button @click="toggleVisibility" class="visibility-test"><img :src="imagemAtual" class="imagem-atual" alt="ImagemNova"></button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imagemAtual: 'https://cdn.discordapp.com/attachments/1097269478280142931/1109174117074227300/eye-icon1.png',
      inputText: '',
      hideText: false,
      inputType: 'password'
    };
  },
  methods: {

    alternarImagem() {
      if (this.imagemAtual === 'https://cdn.discordapp.com/attachments/1097269478280142931/1109174117074227300/eye-icon1.png') {
        this.imagemAtual = 'https://cdn.discordapp.com/attachments/1097269478280142931/1109178628199153764/eye-icon1.png';
      } else {
        this.imagemAtual = 'https://cdn.discordapp.com/attachments/1097269478280142931/1109174117074227300/eye-icon1.png';
      }
    },
    toggleVisibility() {
      this.hideText = !this.hideText;
      this.inputType = this.hideText ? 'text' : 'password';
    }
  }
}




</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.create-account {
  position: absolute;
    color: rgb(91, 91, 250);
    margin-top: 389px;
    z-index: 1;
    text-decoration: none;
    font-weight: 100;
    margin-left: 622px;
    font-family: Arial;
    font-size: 13px;
}

.create-account:hover {
  text-decoration: underline;
}
.pagina-de-registro {
  width: 310px;
    height: 53px;
    border-radius: 7px;
    margin-top: 369px;
    background-color: white;
    position: absolute;
    margin-left: 461px;
    border: 1px solid rgb(221, 221, 221);
}

.umbrella-corp-img {
  position: absolute;
    width: 180px;
    margin-left: 526px;
}
  .teste {
    color: black;
    display: block;
    opacity: 0;
    font-size: 3vw;
    font-family: 'Courier New', Courier, monospace;
    margin-left: 32vw;
  }
  .imagem-atual {
    width: 10px;
    position: absolute;
    margin-top: -5px;
    margin-left: -5px;
  }
  .text-password {
    margin-top: 89px;
    position: absolute;
    font-family: Arial;
    font-weight: 100;
    font-size: 13px;
    margin-left: 37px;
  }

  .pagina-de-login {
    width: 24vw;
    margin-top: 12vw;
    border-radius: 7px;
    margin-left: 36vw;
    height: 16vw;
    background-color: whitesmoke;
    border: 1px solid rgb(221, 221, 221);
  }

  .input-password {
    padding: 5px 12px;
    font-size: 14px;
    line-height: 20px;
    border-radius: 5px;
    width: 17vw;
    margin-top: 107px;
    position: absolute;
    border: 1px solid rgb(201, 201, 201);
    margin-left: 35px;
  }

  .username {
    padding: 5px 12px;
    font-size: 14px;
    line-height: 20px;
    border-radius: 5px;
    width: 17vw;
    margin-top: 43px;
    position: absolute;
    border: 1px solid rgb(201, 201, 201);
    margin-left: 35px;

  }

  .username-text {
    margin-top: 22px;
    margin-left: 35px;
    position: absolute;
    font-size: 13px;
    font-family: Arial;
  }
  .visibility-test {
    width: 1.3vw;
    height: 1.3vw;
    border: 1px solid white;
    background-color: white;
    position: absolute;
    border-radius: 4px;
    margin-left: 20vw;
    margin-top: 9vw;
  }

  .button-confirmed {
    position: absolute;
    width: 19vw;
    margin-left: 35px;
    color: white;
    font-weight: 700;
    box-shadow: 0 1px 0 rgba(31,35,40,0.04);
    font-family: Arial;
    line-height: 25px;
    margin-top: 152px;
    border: 1px solid #1f6e35d2;
    border-radius: 4px;
    transition: 0.25s;
    background-color: #1f883d;
  }

  .button-confirmed:hover {
    background-color: #1b6e32;
  }

  .forgot-password {
    position: absolute;
    background: none;
    border: none;
    margin-top: 88px;
    font-size: 12px;
    font-family: Arial;
    /* text-decoration: underline; */
    color: rgb(91, 91, 250);
    margin-left: 174px;
  }

  .umbrella-corporation {
    position: absolute;
    font-family: Arial;
    margin-top: 389px;
    z-index: 1;
    color: black;
    margin-left: 515px;
    font-size: 13px;
    font-weight: 100;
  }
</style>
