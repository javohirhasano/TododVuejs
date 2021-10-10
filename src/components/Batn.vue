<template>
  <div>
    <button v-on="onClick()" :style="{background:color}" class="btn btn-dark">main</button>
  </div>
</template>

<script>
export default {
    name:"Batn",
    props:{
        text:String,
        color:String
    },
    methods:{
        onClick(){
    console.log('click')
        }
    }
}
</script>
<style>
.btn {
  display: none;
}
</style>