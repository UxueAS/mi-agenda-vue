<template>
  <div class="todo-list">
    <h2>Lista de tareas</h2>
    <div class="row">
      <div class="col-md-8">
        <input type="text" class="form-control" v-model="nuevaTarea" placeholder="Añadir nueva tarea">
      </div>
      <button class="btn btn-primary col-md-4">Añadir tarea</button>
    </div>

    <div v-for="tarea in tareas" :key="tarea.id" class="event">
      <h3>{{ tarea.title }}</h3>
      <p>{{ tarea.date }}</p>
      <p>{{ tarea.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  components: {},
  data() {
    return {
      nuevaTarea: '',
      tareas: [
        { id: 1, title: 'Tarea 1', date: '2023-10-01', description: 'Descripcion de la tarea 1', check: false },
        { id: 2, title: 'Tarea 2', date: '2023-10-02', description: 'Descripcion de la tarea 2', check: true },
        { id: 3, title: 'Tarea 3', date: '2023-10-03', description: 'Descripcion de la tarea 3', check: false },
        { id: 4, title: 'Tarea 4', date: '2023-10-04', description: 'Descripcion de la tarea 4', check: true },
        { id: 5, title: 'Tarea 5', date: '2023-10-05', description: 'Descripcion de la tarea 5', check: false },
        { id: 6, title: 'Tarea 6', date: '2023-10-06', description: 'Descripcion de la tarea 6', check: true },
        { id: 7, title: 'Tarea 7', date: '2023-10-07', description: 'Descripcion de la tarea 7', check: false },
        { id: 8, title: 'Tarea 8', date: '2023-10-08', description: 'Descripcion de la tarea 8', check: true },
        { id: 9, title: 'Tarea 9', date: '2023-10-09', description: 'Descripcion de la tarea 9', check: false },
        { id: 10, title: 'Tarea 10', date: '2023-10-10', description: 'Descripcion de la tarea 10', check: true }
      ],
    };
  }
};
</script>

<style scoped>
.events-calendar {
  padding: 20px;
}

.event {
  margin-bottom: 20px;
}

.event h2 {
  margin: 0;
}

.event p {
  margin: 5px 0;
}
</style>