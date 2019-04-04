<template>
  <div>
    <input v-model="inputValue"/>
    <button @click="tianjia">添加</button>
    <ul>
      <!-- <li v-for="(item,index) in list" v-key="index">{{item}}</li> -->
      <todo-item  v-for="(item,index) in list" :key="item" :content="item" :index="index" @zidel="delMethod"></todo-item>
    </ul>
  </div>
</template>

<script>
import TodoItem from './components/TodoItem.vue'

export default {
  components:{
    'todo-item':TodoItem
  },
  data(){
    return {
      inputValue:"dahai",
      list:[]
    }
  },
  methods:{
    tianjia(){
      this.list.push(this.inputValue);
    },
    delMethod(index){
      this.list.splice(index,1);
    }
  }
}
</script>

<style>

</style>
