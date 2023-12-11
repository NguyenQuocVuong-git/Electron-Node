<template>
  <div class="table-wrapper">
    <table class="table">
      <thead>
        <tr>
          <th>Name</th>
          <th>Age</th>
          <th>Email</th>
          <th>Phone</th>
          <th>Action</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(person, index) in people" :key="index">
          <td>{{ person.name }}</td>
          <td>{{ person.age }}</td>
          <td>{{ person.email }}</td>
          <td>{{ person.phone }}</td>
          <td>
            <button @click="handleClick">Click me</button>
            <button @click="handleClick">Click me</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  component: 'Table',
  data() {
    return {
      people: [
        { name: 'John Doe', age: 30, email: 'mailto:john@example.com', phone: '123-456-7890' },
        { name: 'Jane Smith', age: 25, email: 'mailto:jane@example.com', phone: '987-654-3210' },
      ]
    };
  },
  methods: {
    handleClick: function() {
      alert('Button clicked!');
    }
  }
};
</script>

<style>
.table-wrapper {
  display: flex;
  justify-content: center;
}

.table {
  border-collapse: collapse
}

.table th,
.table td {
  border: 1px solid black;
  padding: 8px;
}
</style>