<template>
<div class="m-3"><h1>ADIL TIME REACTION </h1> <result v-if='isFinished' :Time="timer" :I3ada='I3ada' />
<button @click="start" v-if='!isPlaying' class="btn btn-danger px-5 py-3 mt-5"><h1>{{Play}}</h1> </button>
</div>
   <zone v-if='isPlaying' v-on:fire='Fire($event)' v-on:Zrebty='sirT3awed' /> 
  
</template>

<script>
import zone from './components/zone.vue'
import result from './components/result.vue'
export default {
  name: 'App',
  components: {
    zone,result
  },
  data(){
    return{
        Play:'Start',
        isPlaying:false,
        isFinished:false,
        timer:0,
        I3ada:false,
    }
  },
  methods:{
    start(){
      this.isPlaying=true
      this.isFinished=false
      this.Play='PLAY AGAIN'
    },
    Fire(time){
     this.I3ada=false
      this.timer=time
      this.isPlaying=!this.isPlaying
      this.isFinished=!this.isFinished
            },
    sirT3awed(){
      this.I3ada=true
       this.isPlaying=!this.isPlaying
      this.isFinished=!this.isFinished
            }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align:-webkit-center;
  color: #000000;
  margin: 0;
  padding-top: 100px;
  background-color: blanchedalmond;
  width: 100vw;
  height: 100vh;
}
.app{
  width: 100vw;
  height: 100vh;
  background-color: rgba(146, 173, 226, 0.438);
  text-align: center  !important;
}
</style>
