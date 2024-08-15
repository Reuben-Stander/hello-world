<template>
  <title>My Website</title>
  <header>
    <h1>Welcome to My Website</h1>
  </header>
  <v-btn @click="addLink">Add link</v-btn>
  <nav>
    <ul>
      <li v-for="row in rows">
        <a :href="row.link">{{ row.name }}</a>
      </li>
    </ul>
  </nav>
  <main>
    <h2>About Me</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam euismod
      nibh ac nulla tincidunt, a laoreet nisi malesuada.
    </p>
  </main>
  <footer>&copy; 2022 My Website. All rights reserved.</footer>
</template>

<script setup>
import { ref } from "vue";

let character = "Hello";
let count = 8;
let rows = ref([
  {
    name: "Naomi",
    age: 10,
    link: "https://www.google.com",
  },
  {
    name: "Quincy",
    age: 11,
    link: "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/learn-introductory-javascript-by-building-a-pyramid-generator/step-21",
  },
  {
    name: "CamperChan",
    age: 12,
    link: "https://www.google.com",
  },
]);

function addLink() {
  rows.value.push({
    name: "New Link",
    age: 1,
    link: "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/learn-introductory-javascript-by-building-a-pyramid-generator/step-33",
  });
  count++;
}
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}
header {
  background-color: #333;
  color: white;
  padding: 20px;
  text-align: center;
}
nav {
  background-color: #f4f4f4;
  padding: 10px;
}
nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
nav ul li {
  display: inline;
  margin-right: 10px;
}
main {
  padding: 20px;
}
footer {
  background-color: #333;
  color: white;
  padding: 10px;
  text-align: center;
}
</style>
