<template>
  <AppHeader />
  <br /><br />

  <div class="container">
    <!-- Primera fila -->
    <div class="row">
      <div class="col-md-8 px-2" id="calendario">
        <EventsCalendar />
      </div>
      <div class="col-md-4 px-2" id="contactos">
        <ContactList />
      </div>
    </div>
    <br /><br />

    <!-- Segunda fila -->
    <div class="row mt-4">
      <div class="col-md-7 px-2" id="todo">
        <TodoList />
      </div>
      <div class="col-md-5 px-1" id="notas">
        <NotesList />
      </div>
    </div>
    <br /><br /><br />
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import EventsCalendar from "@/components/EventsCalendar.vue";
import ContactList from "@/components/ContactList.vue";
import TodoList from "@/components/TodoList.vue";
import NotesList from "@/components/NotesList.vue";

export default {
  components: {
    AppHeader,
    EventsCalendar,
    ContactList,
    TodoList,
    NotesList,
  },
};
</script>

<style scoped>
.container {
  margin: 0 auto;
  padding: 0 15px;
}
.row {
  margin-bottom: 1rem;
}

</style>

