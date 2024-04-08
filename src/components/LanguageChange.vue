<template>
    <div>
      <div class="salutation" v-if="language !== ''">
        <div class="frase">{{ $t("salutation.hello") }}</div>
        <div class="hi">{{ $t("salutation.hi") }}</div>
        <div class="goodbye">{{ $t("salutation.goodbye") }}</div>
        <div class="goodmorning">{{ $t("salutation.goodmorning") }}</div>
        <div class="goodafternoon">{{ $t("salutation.goodafternoon") }}</div>
        <div class="goodnight">{{ $t("salutation.goodnight") }}</div>
      </div>
      <div class="change">
        <p class="title-change">Clique na bandeira para alterar o idioma: </p>
        <button @click="changeLanguage('en')">
          <img src="../img/estados-unidos.png" alt="Estatos Unidos">
        </button>
        <button @click="changeLanguage('pt')">
          <img src="../img/brasil.png" alt="Brasil">
        </button>
        <button @click="changeLanguage('sp')">
          <img src="../img/espanha.png" alt="Espanha">
        </button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "LanguageChange",
    data() {
      return {
        language: "",
      };
    },
    methods: {
      changeLanguage(locale) {
        this.language = locale;
        // Altera o idioma no Vue i18n
        this.$i18n.locale = this.language;
      },
    },
  };
  </script>
  
  <style>
  .title-change {
    font-size: 24px;
    text-align: center;
    margin-bottom: 20px;
  }
  
  img {
    width: 100px;
    height: 100px;
    margin: 0 10px;
    cursor: pointer;
  }
  
  img:hover {
    transform: scale(1.2);
  }
  
  .salutation {
    text-align: center;
    margin-top: 50px;
  }
  
  .change {
    text-align: center;
    margin-top: 50px;
  }
  
  .frase {
    font-size: 24px;
  }
  
  .hi {
    font-size: 36px;
  }
  
  .goodbye {
    font-size: 24px;
  }
  
  .goodmorning {
    font-size: 36px;
  }
  
  .goodafternoon {
    font-size: 36px;
  }
  
  .goodnight {
    font-size: 36px;
  }
  
  button {
    margin: 0 10px;
    background-color: transparent;
    border: none;
    cursor: pointer;
  }


  
  </style>
  