<template>
  <form class="add">
    <div class="form-control">
      <label for="text">Ism familiya</label>
      <input type="text" v-model="text" name="text" />
    </div>
    <div class="form-control">
      <label for="text">kun va vaqt</label>
      <input type="day" v-model="day" name="day" />
    </div>
    <div class="form-control form-control-check">
      <label for="text">Tekshirish</label>
      <input class="chek" v-model="checkbox" type="checkbox" value="reminder" />
    </div>
    <button class="batn2">Save Task</button>
  </form>
</template>
<script>
export default {
    name:"AddTask",

  data(){
    return{
      text:"main",
      day:"",
      checkbox:true
  }  
}
}
</script>
<style >
.batn2 {
  width: 100%;
  background-color: black;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 20px;
  box-shadow: 0 10px 10px 2px rgb(149, 204, 241);
}
input {
  width: 100%;
  height: 40px;
  border-radius: 20px;
}
.form-control {
  margin-bottom: 30px;
  font-size: 20px;
  color: rgb(225, 201, 248);
}
.chek {
  margin-right: 400px;
}
.form-control-check {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 20px;
}
</style>