<template>
  <div>
    <div class="containe col-10 col-lg-12 col-md-8">
      <AddTask />
      <div class="input_batn">
        <button @click="AddTask(Addlist)" class="butn">Add-text</button>
      </div>
      <div class="cards" :key="task.id" v-for="task  in tasks">
        <h1 class="write">{{task.text}}</h1>
        <button @click="deletetask(task.id)" class="batn1">delete</button>
      </div>
    </div>
  </div>
</template>

<script>
import AddTask from "./AddTask"

export default {
    name: "Header",
    components:{AddTask},
    props:{
        title:String,tasks:Array
    },

    methods:{
deletetask(v){
    this.$emit("delete-task", v)
},
    },
 emits:["deletetask"]
}
</script>
<style>
body {
  background: rgb(94, 9, 143);
  background: radial-gradient(
    circle,
    rgba(94, 9, 143, 1) 0%,
    rgba(235, 21, 198, 1) 100%
  );
}
header {
  display: flex;
  align-items: center;
}
.write {
  margin-left: 10px;
}
.cards {
  width: 35 0px;
  height: 100px;
  margin-top: 10px;
  background-color: rgb(238, 214, 214);
  margin-left: 20px;
  text-align: center;
  color: red;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.batn1 {
  margin-right: 10px;
  padding: 20px;
  border-radius: 20px;
}
.containe {
  width: 600px;
  height: 840px;
  border: 2px solid black;
  margin-top: 10%;
  margin-left: 10%;
  padding: 10px 20px;
  border-radius: 20px;
  background: rgb(51, 71, 198);
  background: radial-gradient(
    circle,
    rgba(51, 71, 198, 1) 0%,
    rgba(235, 21, 198, 1) 100%
  );
  margin-bottom: 200px;
}
.butn {
  background-color: rgb(82, 185, 185);
  width: 100px;
  height: 30px;
  border-radius: 10px;
  border: 0;
  cursor: pointer;
  margin-left: 20px;
}
.input_batn {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
div {
  display: inline-block;
}
</style>