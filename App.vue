<template>
  <div id="app">
    <h1>Список дел</h1>
    <p>Всего задач: {{ tasks.length }}</p>
    
    <TaskItem 
      v-for="task in tasks" 
      :key="task.id" 
      :task="task" 
    />
  </div>
</template>

<script>
import TaskItem from './components/TaskItem.vue'

export default {
  name: 'App',
  components: {
    TaskItem
  },
  data() {
    return {
      tasks: [
        { id: "1", title: "Изучить Vue", text: "Освоить Vue.js" },
        { id: "2", title: "Создать приложение", text: "Разработать список дел" },
        { id: "3", title: "Выложить на GitHub", text: "Загрузить проект в репозиторий" },
        { id: "4", title: "Изучить TypeScript", text: "Понять основы TypeScript" }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}
</style>