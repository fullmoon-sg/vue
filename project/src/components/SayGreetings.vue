<template>
    <div>
    <h1>{{message}}</h1>
    <button v-on:click ="sayhi">Say Hi</button>
    <button v-on:click="SayGood">Goodbye World</button>
    <button v-on:click="sleep">Sleep</button>
    </div>
</template>

<script>
export default {
    data : function(){
       return {
            'message' : ""
       }
    },props:['g_message'],
    methods : {
        'sayhi' : function(){
            this.message = "Welcome World!"
        },
        'SayGood' : function(){
            this.message= "Goodbye World"
        },
        'sleep' : function(){
            this.message = "Zzz...zzzz"
        }
    }
}

</script>

<style scoped>

</style>