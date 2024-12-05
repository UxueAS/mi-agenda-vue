<template>
  <AppHeader />
  <div class="container">
    <div class="row mt-4">
      <div class="col-md-4 border-end px-2">
        <EventsCalendar />
      </div>
      <div class="col-md-4 border-end px-2">
        <TodoList />
      </div>
      <div class="col-md-4">
        <div class="row">
          <ContactList />
        </div>
        <hr>
        <div class="row px-2">
          <NotesList />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader'
import EventsCalendar from './components/EventsCalendar'
import TodoList from './components/TodoList'
import ContactList from './components/ContactList'
import NotesList from './components/NotesList'
export default {
  name: 'App',
  components: {AppHeader, EventsCalendar, TodoList, ContactList, NotesList}
}
</script>
