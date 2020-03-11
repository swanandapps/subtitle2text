<template>
  <div class="hello">
   
   <div id="compiler">
   <div id="textarea">
    <textarea v-model="subtitle" type="text" name="subtitle" id="subtitlearea"></textarea>

    <button id="subm" @click="RUN()">RUN</button>
   
   </div>

    <div id="output">

<div id="bharatDIV">
        
{{this.output}}

</div>


    </div>
</div>
   

    </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',

data() {
  return {
    
subtitle:this.subtitle,
output:''

  }
},
  props: {
    msg: String
  }

,
methods: {
  
RUN: function()
{

var subtitle=this.subtitle
  

console.log(subtitle.length)




for(var i=0;i<subtitle.length;i++)
{

if(subtitle[i]=='[')
{


  while(subtitle[i]!=']')
  {

i++;


  }


}

else
{


this.output=this.output+subtitle[i]

}


}



}

}
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#bharatP{


text-align: left;
  display: table-cell;
    font-family: monospace
}
#versionNumber{


text-align: left;
  display: table-cell;
    font-family: monospace;
    padding-left: 6%
}

#bharatDIV{

    padding-top: 2%;
    padding-left: 2%;
    overflow: auto;
max-height: 100vh;
background-color: black;
padding-bottom: 5%

}

#linebylineOutput
{



height: 10px;
    text-align: left;
    


}
#errorstack{

text-align: left;
padding-left: 2.5%;
padding-top: 6%;
font-weight: bold;
color:rgb(231, 83, 83);

}

#compiler{

  display: flex;
}

#textarea{

  width: 50%
}
#output{

  height: 400px;
  width: 50%;
  
    color: white;
  
}
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

.hello {
  display: grid;
}

#subtitlearea {
  width: 90%;
  height: 400px;
  background-color: whitesmoke;
    font-family: monospace;
    font-size: medium;
    border: none
}

#subm {
  width: 10%;
  height: 50px;
}
</style>
