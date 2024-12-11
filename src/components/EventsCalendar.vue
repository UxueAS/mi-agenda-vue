<template>
  <div class="events-calendar">
     <h2 class="title">CALENDARIO</h2>
     <div class="calendario">
    <FullCalendar :options="calendarOptions" />

    <div v-for="event in events" :key="event.id" class="event">
      <h2>{{ event.title }}</h2>
      <p>{{ event.date }}</p>
    
    </div>
  </div>
  </div>
</template>



<style>
.title {

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



.calendario {

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
  background-color: #fcebd0;
  z-index: 1;
  position: relative,

}

#task {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 20px;
}

.event {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.full-callendar {
  font-weight: bolder;
}

.event h4 {
  font-size: larger;
  font-weight: bold;
  margin: 0;
  color: #4a4a4a;
}

.event p {
  margin: 5px 0;
  color: #7b9e87;

}

</style>


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