<template>
  <ul class="list-group">
      <li class="list-group-item" v-for="(list,index) in lists">
          <span v-bind:class="{complete:list.complete}">{{list.title}}</span>
          <button @click="delList(index)" class="btn btn-danger btn-xs pull-right">删除</button>
          <button @click="completeList(list)" class="btn  btn-xs pull-right" v-bind:class="[list.complete?'btn-primary':'btn-default']">
            {{list.complete?"完成":"未完成"}}
          </button>

      </li>
  </ul>
</template>
<style>
  .complete{
  color:green;
  text-decoration:line-through;
 }
</style>
<script>
    export default{
      props:['lists'],
        data(){
            return{
                msg:'hello vue'
            }
        },
        methods:{

         delList(index){
          this.lists.splice(index,1)
         },

         completeList(item){
          item.complete=! item.complete
         }
       },
        components:{
        }
    }
</script>
