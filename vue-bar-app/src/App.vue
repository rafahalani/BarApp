<template>
  <div id="app">
    <Form v-form v-on:submit="sub" action="#" method="post"/>
    
  </div>
</template>

<script>
import Form from './components/Form.vue'


export default {
  name: 'App',
  components: {
    Form
  },
  data() {
    return {
      form: []
    }
  },
  methods: {
     /*  sub: function(event){
          
          if(this.login == "" || this.senha == ""){
            this.alert = true
            this.log = "User and Password is required."
            event.preventDefault()
          }else{
            this.log = "Go"
          }   
      } */
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
</style>
