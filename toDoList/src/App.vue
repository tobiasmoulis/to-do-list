<script setup>
import { ref } from 'vue'


let name;
let task;
const tasks = ref([]);

function addTask() {

  if(name == undefined || task == undefined){
    alert('Put in text')
  }
  else{
    tasks.value.push([name,task])
  }
  task = undefined;
  name = undefined;
}

function done(r){
  tasks.value.splice(r, 1);
}
</script>

<template>
  <div class="Page">
    <div class="Header">
      <h1>YOUR TO DO LIST</h1>
    </div>
    <div class="items">
      <div class="item" v-for="(task, index) in tasks">
        <h2>{{ task[0] }}</h2>
        <h3>{{ task[1] }}</h3>
        <button @click="done(index)">DONE</button>
      </div>
    </div>
    <div class="addTask">
    <input v-model="name" placeholder="Task name">
    <textarea v-model="task" name="" cols="30" rows="10" placeholder="Task"></textarea>
    <button @click="addTask">ADD</button>
  </div>
  </div>

  
  
 </template>

<style lang="scss">

@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

/*
*  html5resetcss
*/
html,body,div,span,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,abbr,address,cite,code,del,dfn,em,img,ins,kbd,q,samp,small,strong,sub,sup,var,b,i,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,figcaption,figure,footer,header,hgroup,menu,nav,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;outline:0;font-size:100%;vertical-align:baseline;background:transparent}
body{line-height:1}
article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}
nav ul{list-style:none}
blockquote,q{quotes:none}
blockquote:before,blockquote:after,q:before,q:after{content:none}
a{margin:0;padding:0;font-size:100%;vertical-align:baseline;background:transparent}
ins{background-color:#ff9;color:#000;text-decoration:none}
mark{background-color:#ff9;color:#000;font-style:italic;font-weight:bold}
del{text-decoration:line-through}
abbr[title],dfn[title]{border-bottom:1px dotted;cursor:help}
table{border-collapse:collapse;border-spacing:0}
hr{display:block;height:1px;border:0;border-top:1px solid #ccc;margin:1em 0;padding:0}
input,select{vertical-align:middle}

button{
    all: unset;
    background-color: rgba(253, 182, 105, 1);
    border-radius: 10px;
}
button:hover{
  background-color: darken(rgba(253, 182, 105, 1), 5);
}

.addTask{
  display: flex;
  flex-direction: column;
  gap: 3vh;
  align-items: center;
  padding: 0vh 0vh;
  font-size: 1.5rem;
  padding: 2vh 0vw;
  input{
    width: 30%;
    border: none;
    border-radius: 10px;
    padding: 1vh 2vw;
    font-weight: 700;
    height: fit-content;
    background-color: rgba(38, 39, 42, 1);
    color: white;
  }
  textarea{
    width: 30%;
    border: none;
    border-radius: 10px;
    padding: 1vh 2vw;
    font-weight: 700;
    background-color: rgba(38, 39, 42, 1);
    color: white;
  }
  button{
    padding: 1vh 2vw;
    font-weight: 700;
  }
}
.items{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  height: 50vh;
  max-width: 100%;
  padding: 0vh 2vw;
  overflow-y: scroll;
  row-gap: 2vh;
  .item{
    background-color: rgba(38, 39, 42, 1);
    border-radius: 10px;
    width: 20vw;
    height: fit-content;
    display: flex;
    flex-direction: column;
    word-wrap: break-word;
    padding: 2vh;
    text-align: center;
    gap: 1.5vh;
    align-items: center;
    h2{
      font-size: 1.5rem;
      text-align: center;
      color: rgba(253, 182, 105, 1);
      width: 100%;
    }
    h3{
      color: white;
      font-weight: 400;
      width: 100%;
    }
    button{
      margin-top: 1vh;
      font-weight: 600;
      width: fit-content;
      padding: 1vh 2vw;
    }
  }
}
.Page{
  background-color: #08090B;
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  font-family: 'Roboto', sans-serif;
}
.Header{
  padding: 1vh 0vw;
   width: 100%
};
h1{
color: #FDB669
}
h1{
text-align: center; 
justify-content: center;
font-size: 4rem;}

@media screen and (max-width: 800px) {
  .items{
    grid-template-columns: 1fr 1fr;
    .item{
      width: 38vw;
    }
  }
  h1{
    font-size: 2rem;
  }
  .addTask{
    input{
      width: 70%;
    }
    textarea{
      width: 70%;
    }
    button{
      padding: 1vh 10vw;
    }
  }
}

</style>
