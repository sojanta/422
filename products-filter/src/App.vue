<template>
  <div class="app">
    <header class="app-header">
      <h1>Список дел</h1>
    </header>

    <main class="tasks-container">
      <div class="tasks-list">
        <TaskItem v-for="task in tasks" :key="task.id" :task="task" />
      </div>
    </main>
  </div>
</template>

<script>
import TaskItem from "./components/TaskItem.vue";

export default {
  name: "App",
  components: {
    TaskItem,
  },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Сходить в стоматологию",
          text: "Узнать цену лечения зуба.",
        },
        {
          id: 2,
          title: "Сделать домашнее задание",
          text: 'Английский, русский, математика.',
        },
        {
          id: 3,
          title: "Полить цветы у бабушки",
          text: "Не забыть про цветы на кухне и в зале.",
        },
        {
          id: 4,
          title: "Сделать развертку коробки",
          text: "Разверка для льва 20х10х4,5.",
        },
      ],
    };
  },
};
</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Montserrat", sans-serif;
  background-color: #FFFFFF; 
  color: #333;
}

.app {
  max-width: 100%;
  margin: 0 auto;
  padding: 20px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.app-header {
  text-align: center;
  margin-bottom: 30px;
}

.app-header h1 {
  color: #2C3E50;
  font-size: 2.5rem;
  font-weight: bold;
  letter-spacing: 1px;
}

.tasks-container {
  width: 500px;
  max-width: 1000px;
  background: #c3ffa7;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
  padding: 20px;
}

.tasks-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}
</style>