<template>
  <div id="app">
  <MessageBox message="danger danger will Robinson"  bgcolor="orange"></MessageBox>
  <MessageBox message="The jump jump moon and cow" v-bind:bgcolor ="abc"></MessageBox>
 
  <h1>{{text}}</h1>
  <!-- //The v-onn click is like a listener, when the button is clicked, it will look for function under the export-methods -->
  <button v-on:click="buttonPressed">Click</button>
  <input type="text" v-model='abc'/>
  <Light></Light>
   <SayGreetings g_message = "Say Hi"></SayGreetings>
   <nCounter ></nCounter>
  
  </div>

</template>

<script>
import MessageBox from "./components/MessageBox"
import Light from "./components/Light"
import SayGreetings from "./components/SayGreetings"
import nCounter from "./components/nCounter"

export default {
    name: 'App',
    components : {
        MessageBox,Light,SayGreetings,nCounter
    },
    data: function(){
        return {
        'text' : "This is it",
        'abc' : 'azure',
               }
        },
    methods: {
        'buttonPressed': function() {
            this.text = "You clicked me!"
        },
    }
}
</script>

// without scoped, it will be a global background
<style scoped>

div{
    background-color: pink;
}

</style>
