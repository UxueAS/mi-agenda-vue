<template>
  <div class="events-calendar">
    <h2>Calendario</h2>
    <FullCalendar :options="calendarOptions" />
    <div v-for="event in events" :key="event.id" class="event">
      <h2>{{ event.title }}</h2>
      <p>{{ event.date }}</p>
      <p>{{ event.description }}</p>
    </div>
  </div>
</template>

<script>
import FullCalendar from '@fullcalendar/vue3'
import dayGridPlugin from '@fullcalendar/daygrid'
export default {
  name: 'EventsCalendar',
  components: {FullCalendar},
  data() {
    return {
      events: [
        { id: 1, title: 'Event 1', date: '2023-10-01', description: 'Description for event 1' },
        { id: 2, title: 'Event 2', date: '2023-10-02', description: 'Description for event 2' },
        // Add more events here
      ],
      calendarOptions: {
        plugins: [dayGridPlugin],
        initialView: 'dayGridMonth'
      }
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