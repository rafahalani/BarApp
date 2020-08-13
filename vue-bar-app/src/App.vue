<template>
  <div id="app">
    <Form v-on:submit="submit"/>
    
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
    mounted(){
      
    }
  },
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
