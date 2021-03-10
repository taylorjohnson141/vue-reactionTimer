<template>
  <p> {{ score }} ms</p>
  <p>{{ rank }}</p>
</template>

<script>
export default {
  props:["score"],
  data(){
    return {
      rank:null
    }
  },
  mounted(){
    if(this.score < 250){
      this.rank = 'That was fast'
    }else if(this.score < 400){
      this.rank = 'Can you go faster?'
    }else{
      this.rank = 'That was slow Try again!!'
    }
  }
}
</script>

<style>

</style>