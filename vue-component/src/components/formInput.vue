<template>
   <form action="" method="post">
       <div class="form-group">
           <input type="text" class="form-control" v-model="list.title">
       </div>
       <div class="form-group">
           <input class="btn btn-success" type="submit" @click.prevent="add(list)">
       </div>
   </form>
</template>
<style>

</style>
<script>
    export default{
       props:['lists'],
        data(){
            return{
                 list:{id:'','titile':"",complete:false}
            }
        },
        methods:{
        add(list){
           this.lists.push(list);
            this.list={id:'','titile':"",complete:false}
        }
        },

        components:{
        }
    }
</script>
