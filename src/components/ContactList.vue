<template>
  <div class="contacts">
    <h2>CONTACTOS</h2>
    <ul>
      <li v-for="contact in contacts" :key="contact.id">
        {{ contact.name }} - {{ contact.email }}
            </li>
          </ul>
        </div>
      </template>



<style scoped>
.contacts {
  padding: 10px;

  font-family: 'courier', 'Georgia', serif;
  font-weight: 600;
  margin: 10px;
  margin-top: 0px;

  border-radius: 8px;
  box-shadow: 6px 2px 5px rgba(0, 0, 0, 0.374);
  background-color: #a4b8aba0;
}



.contacts ul {
  list-style: disc;
  margin: 5px 10px;
  margin-top: 20px;
  padding: 20px;
}

.contacts li {
  margin-bottom: 10px;
  font-size: 0.9em;
  color: #4a4a4a;

}


.contacts h2 {
  color: #7e7666;
  padding: 5px;
  border-radius: 5px;
  background-color: #e0dad180;
  box-shadow: inset 0 4px 8px rgba(0, 0, 0, 0.1);
  font-weight: bold;
  text-align: center;
  margin-top: 10px;
}

.contacts ul li:hover {
  color: #c28d42;
  text-decoration: underline;
}
</style>


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

