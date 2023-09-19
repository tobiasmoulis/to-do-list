<script setup>

let name;

function addTask() {
  alert(name)
}
</script>

<template>
  <div class="addTask">
    <input v-model="name" placeholder="Název úkolu">
    <input type="text" placeholder="Počet úkolů">
    <button @click="addTask">Vytvořit</button>
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
</style>
