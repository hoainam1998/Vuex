<template>
  <div>
    <h3>todos</h3>
    <div class="todos">
        <div v-for="todo in allTodos" :key="todo.id" class="todo">{{todo.title}}</div>
    </div>
  </div>
</template>
<script>
import {mapGetters} from 'vuex'
export default {
    name: "Todo",
    computed: mapGetters(['allTodos'])
};

</script>
<style scoped>
.todos {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 1rem;
}
.todo {
  border: 1px solid #ccc;
  background: #41b883;
  padding: 1rem;
  border-radius: 5px;
  text-align: center;
  position: relative;
  cursor: pointer;
}
</style>