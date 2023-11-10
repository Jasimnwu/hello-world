<template>
 <div :id="headingid" :class="wrap" >{{ hello }} {{ name }}</div>
 <span v-html="ceo"></span>
 <button :disabled="isButtonDisabled" >Hello</button>
 <div v-bind:class="isactive?'active': 'deactive'" >Hello active class</div>
 <div v-bind:class="[promoto &&'promoto',valueactive ? 'valueactive':'deactive']" >Hello active class</div>
 <h2 :style="styleObject" >HilightColor</h2>
 <button @click="awesome = !awesome">Toggle</button>
 <h1 v-if="awesome">Vue is awesome!</h1>
 <h1 v-else>Oh no 😢</h1>
 <h1 v-if="num == 0" >Number is {{num}}</h1>
 <h1 v-else>Number is {{num}}</h1>
 <ul>
  <li v-for="list in booklist" :key="list" >{{ list }}</li>
 </ul>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      hello:"Hello",
      name:"Sagor",
      ceo:'<b>CEO</b>',
      headingid:"headingind",
      isButtonDisabled:false,
      wrap:"wrap",
      isactive:false,
      promoto:false,
      valueactive:true,
      styleObject:{
        color:"#FF6000",
        padding:'10px'
      },
      awesome:'awesome',
      num:5,
      booklist:['Book1','Book2','Book3']
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.active {
  color: #1640D6;
}
.deactive {
  color: #B31312;
}
.promoto {
  font-style: italic;
}
.valueactive {
  color: rebeccapurple;
}
</style>
