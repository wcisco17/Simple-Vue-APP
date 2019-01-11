<template>
  <div class="home">

    <div class="world" >
    <Todo v-bind:todos="todos"  />
    </div>
  </div>
</template>

<script>
  // @ is an alias to /src
  import HelloWorld from "@/components/HelloWorld.vue";
  import Todo from "@/components/Todo.vue";



  export default {
    name: "home",
    components: {
      HelloWorld,
      Todo
    },
    data() {
      return {
        todos: [
          {
            id: 1,
            title: "First Todo",
            completed: false
          },
          {
            id: 2,
            title: "Second Todo",
            completed: true
          },
          {
            id: 3,
            title: "Third Todo",
            completed: false
          }
        ]
      }
    }
  };
</script>


<style scoped>
  .home {
    display: flex;
    align-items: center;
    justify-content: center;
    grid-area: home;
  }


  
</style>