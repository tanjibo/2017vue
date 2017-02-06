<template>
    <div id="app" class="container">
        <div class="panel panel-default">
             <div class="panel-heading">
                 <h3 class="panel-title">vue-cli 练习</h3>
             </div>
            <div class="panel-body">
                <form-list v-bind:lists="lists"></form-list>
                <form-input v-bind:lists="lists"></form-input>
            </div>
        </div>

    </div>
</template>

<script>
import FormList from './components/FormList'
import FormInput from './components/FormInput'


export default {
  name: 'app',
  data(){
    return{
    lists:[{'id':'1','title':'first one','complete':false}],

    }
  },
  components: {
    'form-list':FormList,
    'form-input':FormInput
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
