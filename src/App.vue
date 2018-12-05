<template>
  <div id="app">
    <img src="./assets/logo.png">
    <test1/>
    <h3>{{ClassNam}}</h3>
    <h4>{{stud.FirName}}</h4>
    <h5>{{stud.Grade}}</h5>

   <h1>The following are V text Directives </h1>
   <p v-text="stud.FirName"></p>

   <p v-if="conditionval">if true: {{stud.FirName}}</p>
   <p v-else="conditionval">Condition val is false</p>

<ul>

<li v-for="mk in marks">{{mk.mark1}}</li>
</ul>
  </div>
</template>

<script>
import test1 from './components/test'

export default {
  name: 'App',

  components: {
    test1
  },
   data()
  {
    return{
      ClassNam:'Class 2',
      stud:{
          FirName:'Sam',
          Grade :'A grade'
      },
      conditionval: false,
      marks:[
        {mark1:'100'},
        {mark1:'90'},
        {mark1:'77'},
        {mark1:'45'},
      ]
      }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
