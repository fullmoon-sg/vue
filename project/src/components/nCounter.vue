<template>
<div>
   <div class="container">
    <div>
        {{number}}
    </div>
    <div>
        <span v-if = "number%2 == 0" style.color="green">Even</span>
        <span v-else color="red"> Odd</span>
    </div>
    <button v-on:click="increase">Increase</button>
    <button v-on:click ="decrease">Decrease</button>
    </div>
</div>
</template>

<script>
export default {
    data : function(){
        return{
            number : 0,
            bgcolor : "",
        }
    },
    methods : {
        'increase' : function(){
            this.number += 1
        },
        'decrease' : function(){ 
            this.number -= 1
        }
    }

    
}
</script>

<style scoped>



</style>