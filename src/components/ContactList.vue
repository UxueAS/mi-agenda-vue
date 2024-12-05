<template>
  <div class="contacts">
    <h1>Contact List</h1>
    <ul>
      <li v-for="contact in contacts" :key="contact.id">
        {{ contact.name }} - {{ contact.email }}
            </li>
          </ul>
        </div>
      </template>

<script>
  export default {
    name: 'ContactList',
    data() {
      return {
        contacts: [
          { id: 1, name: 'John Doe', email: 'john.doe@example.com' },
          { id: 2, name: 'Jane Smith', email: 'jane.smith@example.com' },
          { id: 3, name: 'Alice Johnson', email: 'alice.johnson@example.com' },
          { id: 4, name: 'Bob Brown', email: 'bob.brown@example.com' },
          { id: 5, name: 'Charlie Davis', email: 'charlie.davis@example.com' },
          { id: 6, name: 'Diana Evans', email: 'diana.evans@example.com' },
          { id: 7, name: 'Evan Harris', email: 'evan.harris@example.com' },
          { id: 8, name: 'Fiona Green', email: 'fiona.green@example.com' },
          { id: 9, name: 'George King', email: 'george.king@example.com' }
        ]
      };
    }
  };
</script>

<style scoped>
.contacts {
  padding: 20px;
}

.contacts h1 {
  font-size: 24px;
  margin-bottom: 10px;
}

.contacts ul {
  list-style-type: none;
  padding: 0;
}

.contacts li {
  padding: 5px 0;
}
</style>