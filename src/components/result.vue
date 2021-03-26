<template>
  
    <div v-if="I3ada" class="bg-warning text-center ">
        <h3>You clicked Too Early try again</h3>
    </div>
      <div v-else class="bg-dark text-center ">
        <h3>Your result is :</h3>
        <h1>{{Time}} ms</h1>
    </div>
</template>
<script>
export default {
    props:['Time','I3ada'],
  data(){
      return{
         
      }
  }
}
</script>
<style >
.text-center{
    color: blanchedalmond;
}
</style>