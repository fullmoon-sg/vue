<template>
<div>
    <div v-if = "switchStatus == true">
        Lights On
    </div>
    <div v-else>
        Light is off
    </div>
    <button v-on:click="toggleLight">Toogle</button>
</div>    
    
</template>

<script>
export default {
    data: function(){
        return {
            'switchStatus' : false
        }
    },
    props:[],
    methods: {
        'toggleLight' : function(){
            this.switchStatus = !this.switchStatus;
        }
    }
    
}
</script>

<style scoped>


</style>