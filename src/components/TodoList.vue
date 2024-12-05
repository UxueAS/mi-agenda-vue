<template>
  <div class="todo-list">
    <h2>Lista de tareas</h2>
    <div class="row mb-4">
      <div class="col-md-8">
        <input type="text" class="form-control" v-model="nuevaTarea" placeholder="Añadir nueva tarea">
      </div>
      <div class="col-md-4"><button @click="agregarTarea" class="btn btn-primary">Añadir tarea</button></div>

    </div>

    <div v-for="tarea in tareasPendientes" :key="tarea.id" class="event">
      <div class="row">
        <div class="col-1">
          <input type="checkbox" v-model="tarea.check">
        </div>
        <div class="col-11">
          <p>{{ tarea.date }} | <span class="fw-bold">{{ tarea.title }}</span></p>
        </div>
      </div>
    </div>
    <hr>
    <div v-for="tarea in tareasCompletadas" :key="tarea.id" class="event">
      <div class="row">
        <div class="col-1">
          <input type="checkbox" v-model="tarea.check">
        </div>
        <div class="col-11">
          <p>{{ tarea.date }} | <span class="fw-bold">{{ tarea.title }}</span></p>
        </div>
      </div>
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
  },
  computed: {
    tareasPendientes() {
      return this.tareas.filter(tarea => !tarea.check);
    },
    tareasCompletadas() {
      return this.tareas.filter(tarea => tarea.check);
    }
  },
  methods: {
    agregarTarea() {
      this.tareas.push({
        id: this.tareas.length + 1,
        title: this.nuevaTarea,
        date: new Date().toISOString().substr(0, 10),
        description: 'Descripción de la tarea',
        check: false
      });
      this.nuevaTarea = '';
    }
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

.event h3 {
  margin: 0;
  font-size: 20px;
}

.event p {
  margin: 0;
}
</style>