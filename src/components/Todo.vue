<template>
    <div>
        <h2>Todo App</h2>
        <div v-bind:key="todo.id" class="todo" v-for="todo in todos" >
            <h3> {{ todo.id }}: {{ todo.title }}</h3>
       </div>   
    </div>    
</template>


<script>
export default {
    name: "Todo",
    props: ['todos'],
}
</script>


<style scoped>
    .todo {
        text-align: center;
        padding-top: 2rem;
    }

</style>
