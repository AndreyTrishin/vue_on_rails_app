<template>
  <div id="app">
    <p>{{ message }}</p>
    <input type="text" v-on:change="message = newMessage" v-model="newMessage" />
    <table class="table">
      <thead>
        <tr>
          <th>Имя</th>
          <th>Описание</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in table" v-bind:key="item.id">
          <td>{{item.name}}</td>
          <td>{{item.description}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
var f = "sdafasdfasdf";
export default {
  data: function() {
    return {
      message: f,
      table: [
        { id: 1, name: "Item 1", description: "Description 1" },
        { id: 2, name: "Item 2", description: "Description 2" },
        { id: 3, name: "Item 3", description: "Description 3" },
        { id: 4, name: "Item 4", description: "Description 4" },
        { id: 5, name: "Item 5", description: "Description 5" },
        { id: 6, name: "Item 6", description: "Description 6" },
        { id: 7, name: "Item 7", description: "Description 7" }
      ]
    };
  }
};
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
