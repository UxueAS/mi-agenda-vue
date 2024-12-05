<template>
  <div class="notes-list">
    <h2>Notas</h2>
    <ul>
      <li v-for="note in notes" :key="note.id">
        {{ note.text }}
      </li>
    </ul>
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
        { id: 3, text: 'Nota 3' }
      ]
    };
  }
};
</script>

<style scoped>
.notes-list {
  padding: 20px;
  background-color: #f9f9f9;
}

.notes-list h2 {
  margin-bottom: 10px;
}

.notes-list ul {
  list-style-type: none;
  padding: 0;
}

.notes-list li {
  padding: 10px;
  border-bottom: 1px solid #ddd;
}
</style>