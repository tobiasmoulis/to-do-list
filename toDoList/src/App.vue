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

.addTask{
  display: flex;
  flex-direction: column;
  gap: 3vh;
  align-items: center;
  padding: 0vh 0vh;
  font-size: 1.5rem;
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
    padding: 1vh 2vw;
    font-weight: 700;
  }
  button:hover{
    background-color: darken(rgba(253, 182, 105, 1), 10);
  }
}
.Page{
  background-color: #08090B;
  height: 100vh;
  width: 100vw;
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
justify-content: center;
font-size: 4rem;}

</style>
