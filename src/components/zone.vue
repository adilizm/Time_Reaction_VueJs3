<template>
     <div v-if='!Start_Counting' class="zone" @click='ToEarly' >
        <h1>Wait for the red <br> BE REDY</h1> 
     </div>
     <div class="redzone" v-if='Start_Counting' @click="FireO" ></div>
</template>


<script>
export default {
       
  data(){return{
        Start_Counting:false,     
        timer1:0 ,
        interval:null,
    }},
    props:['Play'],
    methods:{
      ToEarly(){
           this.$emit('Zrebty')
      },
      FireO(){
       
        clearInterval(this.interval)
        this.$emit('fire',this.timer1)
      }
    },
   mounted(){
     setTimeout( ()=>{
         this.Start_Counting=true
         this.interval = setInterval(() => { this.timer1+=10 }, 10);


     },1000+Math.random()*7000 )
  } 
}
</script>
<style>
.zone{
    background-color: aquamarine;
    width: 70%;
    height: 300px;
    border-radius: 10px;
    text-align: center;
   font-size:40px;
}
.zone h1{
    font-family: 'Courier New', Courier, monospace;
    padding-top: 30px;
}
.redzone{
     background-color: rgb(255, 0, 0);
      width: 70%;
    height: 300px;
    border-radius: 10px;
    text-align: center;
   font-size:40px;
}
</style>