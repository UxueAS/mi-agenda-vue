

<template>
  <div class="stiker">
    <h2>NOTAS</h2>
    <div class="notas">
      <div v-for="note in notes" :key="note.id">
        <p>{{ note.text }}</p>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'NotesList',
  data() {
    return {
      notes: [
        { id: 1, text: 'Nota 1' },
        { id: 2, text: 'Nota 2' },
        { id: 3, text: 'Nota 3' },
        { id: 4, text: 'Nota 4' }
      ]
    };
  }
};
</script>

<style scoped>

.stiker {
  font-family: 'courier', 'Georgia', serif;
  font-weight: 600;
  margin: 10px;
  padding: 10px;
  border-radius: 8px;
  box-shadow: 6px 2px 5px rgba(0, 0, 0, 0.374);
  background-color: #a4b8aba0;
}


h2 {
  color: #7e7666;
  text-align: center;
  padding: 5px;
  margin: 5px;
  background-color: #a1b5a875;
  border-radius: 5px;
  box-shadow: inset 4px 4px 4px rgba(0, 0, 0, 0.23);
  font-weight: bold;
  margin-top: 10px;
}


.notas {
  font-family: 'courier', 'Georgia', serif;
  padding-top: 10px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 7px;
  width: 100%;
  justify-content: center;
}


.notas div {
  background-color: #fcebd0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  border-radius: 0 0 3px 3px;
  padding: 10px;
  margin: 5px;
  margin-bottom: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.459);
  min-width: 100px;
  max-width: 250px;
  height: 150px;
}
</style>