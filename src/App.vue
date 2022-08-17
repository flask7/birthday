<template>
  <v-app elevation="0">
    <v-app-bar
      app
      elevate-on-scroll
      color="#222"
      dark
    >
      <h1>¡Felíz cumpleaños Vladi!</h1>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>

<style>

  .v-main {
    background: #222;
  }

  * {
    box-sizing: border-box;
  }

  .v-sheet.v-app-bar.v-toolbar:not(.v-sheet--outlined) {
    box-shadow: none;
    border: none;
  }

  h1 {
    width: 100%;
    text-align: center;
    animation-name: hp;
    animation-duration: 320ms;
  }

  @import url('https://fonts.googleapis.com/css?family=Pacifico');

  body{
    background-color: #222;
  }

  @-webkit-keyframes blinkH1 {
      0%   {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;
      }
      19%   {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;
      }
      20% {
          color: #9E9E9E;
        text-shadow: none;  
      }
      21% {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;  
      }
      60% {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;  
      }
      61% {
          color: #9E9E9E;
        text-shadow: none;  
      }
      62% {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;  
      }
      63% {
          color: #9E9E9E;
        text-shadow: none;  
      }
      64% {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;  
      }
      100% {
          color: #fff;
        text-shadow: 0px 0px 20px #138861;  
      }
  }

  @-webkit-keyframes blinkH1After {
      0%   {
          color: #138861;
      }
      19%   {
          color: #138861;
      }
      20% {
          color: transparent; 
      }
      21% {
          color: #138861;  
      }
      60% {
          color: #138861;  
      }
      61% {
          color: transparent; 
      }
      62% {
          color: #138861;  
      }
      63% {
          color: transparent; 
      }
      64% {
          color: #138861;  
      }
      100% {
          color: #138861;  
      }
  }

  @-webkit-keyframes blinkH1Before {
      0%   {
          background: #138861;
      }
      19%   {
          background: #138861;
      }
      20% {
          background: transparent; 
      }
      21% {
          background: #138861;  
      }
      60% {
          background: #138861;  
      }
      61% {
          background: transparent; 
      }
      62% {
          background: #138861;  
      }
      63% {
          background: transparent; 
      }
      64% {
          background: #138861;  
      }
      100% {
          background: #138861;  
      }
  }

  h1{
    font-family: 'Pacifico', cursive;
    font-weight: 100;
    margin: 0px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50% ,-50%);
    color: #fff;
    font-size: 50px;
    text-shadow: 0px 0px 20px #138861;
    -webkit-animation: blinkH1 5s  infinite;
    animation: blinkH1 5s  infinite;
  }

  h1:after{
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    color: #138861;
    z-index: -1;
    filter: blur(15px);
    -webkit-animation: blinkH1After 5s  infinite;
    animation: blinkH1After 5s  infinite;
  }

  h1:before{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #138861;
    z-index: -2;
    opacity: 0.7;
    filter: blur(50px);
    -webkit-animation: blinkH1Before 5s  infinite;
    animation: blinkH1Before 5s  infinite;
  }

  h1.txt-by{
    z-index: 2;
    font-size: 30px;
    top: calc(50% - 55px);
  }

  h1.txt-ne{
    top: calc(50% + 5px);
    text-align: center;
    line-height: 1;
    margin-top: 15px;
  }

  @keyframes hp {
    from {
      margin-left: -100%;
      opacity: 0;
    }

    to {
      margin-left: initial;
      opacity: 1;
    }
  }

  @media only screen and (max-width: 768px) {
    h1 {
      font-size: 2em;
    }
  }

</style>