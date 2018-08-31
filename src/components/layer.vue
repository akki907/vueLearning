<template>
<div class="container">
    <h1>Main Component</h1>  
    <div class="form" >
        <div class="form-group">
            <hr>
            <input type="text" v-model="todo" class="form-control" id="todo" a placeholder="Enter Todo.............">
       </div>
       <div v-if="message">{{message}}</div>
      <div>
            <button  class="btn btn-primary" @click="submitHandler" :disabled="!todo">Add</button>
     </div>

    </div>
    <br>
    <ul class="list-group" v-for="(todo, index) in todos" :key="todo.id">
        <li style="margin:10px;" class="list-group-item">{{todo.name}}
          <span><i class="fa fa-trash pull-right btn btn-link" @click="deleteHandler(index)" aria-hidden="true"></i></span>
          
        </li>
    </ul>
</div>
</template>

<script>
export default {
  name: "Layer",
  data() {
    return {
      todo: "",
      message: "",
      todos: [
        { name: "test" },
        { name: "test2" },
        { name: "test2" },
        { name: "test4" }
      ]
    };
  },
  props: {
    testProps: ""
  },
  methods: {
    submitHandler: function() {
      if (this.todo == "") return (this.message = "Todo cannot be Empty");
      this.todos.push({ name: this.todo });
      this.todo = "";
    },
    deleteHandler: index => {
      console.log(index);
      if (index > -1) {
      //  this.todos.splice(index, 1);
       console.log(this.todos)
       }
      // this.todos.splice(i, 1);
    }
  }
};
</script>


<style >
</style>


