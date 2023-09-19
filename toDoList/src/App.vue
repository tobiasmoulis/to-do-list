<script setup>

let name;

function addTask() {
  alert(name)
}
</script>

<template>
  <div class="Page">
    <div class="Header">
      <h1>YOUR TO DO LIST</h1>
    </div>
    <div class="addTask">
    <input v-model="name" placeholder="Název úkolu">
    <input type="text" placeholder="Počet úkolů">
    <button @click="addTask">Vytvořit</button>
  </div>
  </div>

  
  
 </template>

<style lang="scss">
.addTask{
  background-color: black;
  display: flex;
  flex-direction: column;
  gap: 3vh;
  align-items: center;
  padding: 1vh 0vh;
  input{
    width: 30%;
    border: none;
    border-radius: 100px;
    padding: 1vh 2vw;
    font-weight: 700;
    height: fit-content;
    background-color: rgba(38, 39, 42, 1);
    color: white;
  }
  button{
    all: unset;
    background-color: rgba(253, 182, 105, 1);
    border-radius: 100px;
    padding: 1vh 3vw;
    font-weight: 700;
  }
  button:hover{
    background-color: darken(rgba(253, 182, 105, 1), 10);
  }
}
.Page{
  background-color: #08090B;
  height: 100%;
  width: 100%;
  }
.Header{
  height: 40%;
   width: 100%
  };
h1{
color: #FDB669
}
h1{
text-align: center; 
justify-content: center;}

</style>
