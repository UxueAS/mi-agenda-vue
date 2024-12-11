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





<style scoped>


.todo-list {
  font-family: 'courier', 'Georgia', serif;
}


.row {
  background-color: #fcebd0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  margin: 10px;
  margin-top: 0px;
  padding: 10px;
  border-radius: 0 0 8px 8px;
  box-shadow: 0 6px 5px rgba(0, 0, 0, 0.236);
  font-family: 'courier', 'Georgia', serif;
  font-weight: bold;
  z-index: 1;
  position: relative;

}


.nueva {
  text-align: center;
  margin-top: 20px;
  margin-bottom: 10px;

}



.todo-list button {
  padding: 4px 15px;
  background-color: #7b9e87;
  color: white;
  border: none;
  border-radius: 5px;
  font-weight: bold;
}

.todo-list button:hover {
  background-color: #4a4a4a;
}


.todo-list ul li {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
  color: #4a4a4a;

}

.todo-list ul li input[type="checkbox"] {
  margin-right: 10px;
  accent-color: #7b9e87;
  cursor: pointer;

}

.todo-list ul li:hover { 
  color: #7b9e87;
  font-weight: bold;
}


.todo-list h2 {
  font-weight: bold;
  font-family: 'courier', 'Georgia', serif;
  text-align: center;
  position: relative;
  z-index: 2;
  padding-top: 20px;
  padding: 5px;
  color: #7e7666;

  margin: 7px;
  margin-bottom: -10px;
  background-color: #a1b5a8;
  border-radius: 5px 5px 0 0;
  box-shadow: 0 4px 4px rgba(0, 0, 0, 0.364);

  font-weight: bold;
  margin-top: 10px;
}

</style>


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

