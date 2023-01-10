<template>
  <div id="app">
    <h1>Анкетирование</h1>
    
    <hr>
    <h2>Сколько часов вы спите</h2>
    <MyFirstPage 
    v-bind:questions="questions"   
    />

  </div>
</template>

<script>
import MyFirstPage from '@/components/MyFirstPage.vue'
export default {
  name: 'App',
  data(){
    return{
      questions: [
        {id:1, title: 'Вы высыпаетесь?', completed:false},
        {id:2, title: 'Сколько часов вы спите', completed:false},
        {id:3, title: 'Как вы спите', completed:false},
      ]
    }
  },
  components: {
    MyFirstPage
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
  margin-top: 50px;
}
</style>
