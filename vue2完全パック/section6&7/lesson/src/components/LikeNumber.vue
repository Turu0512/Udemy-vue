<template>
 <div>
 <p>いいね（{{halfNumber}}）</p>
 <button @click="incriment">+1</button>
   
 </div>
</template>

<script>
export default{
  props:{
   number:{
    type:Number,
    default:10
   }
  },
  computed:{
   halfNumber(){
    return this.number / 2
   }
  },
  methods:{
    incriment(){
     this.$emit("my-click",this.number+1)
    }
  }
}
</script>

<style scoped>
div{
  border:1px solid red;
}
</style>
