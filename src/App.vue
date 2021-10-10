<template>
  <div class="containes">
    <Batn text="Add-Taxt" color="green" />
    <Header @delete-task="deletetask" :tasks="tasks"></Header>
  </div>
</template>

<script>

import Header from "./components/Header"
import Batn from "./components/Batn"
export default {
  name: "App",
  components: {Header,Batn},
  data(){
    return{
      tasks:[]
    }
  },
  methods:{
    deletetask(id){
      this.tasks=this.tasks.filter((task)=>task.id!==id)
    },

  },
  created(){
    this.tasks=[
      {
        id:1,
        text:"present simple",
        day:"Salom",
        reminder:false
      },
        {
        id:2,
        text:"past simple",
        reminder:false
      },
        {
        id:3,
        text:"future simple",
        reminder:false
      },
    ]
  }
};
</script>

<style>
body {
  width: 100%;
}
button {
  background-color: blueviolet;
  color: aliceblue;
}
</style>
