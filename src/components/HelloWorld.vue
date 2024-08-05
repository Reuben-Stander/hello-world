<template>
<title>My Website</title>
<header>
        <h1>Welcome to My Website</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#">{{rows[2]}}</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    <main>
        <h2>About Me</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam euismod nibh ac nulla tincidunt, a laoreet nisi malesuada.</p>
    </main>
    <footer>
        &copy; 2022 My Website. All rights reserved.
    </footer>
</template>

<script setup>
import { ref } from 'vue'

let character = 'Hello';
let count = 8;
let rows = ref(["Naomi", "Quincy", "CamperChan"]);
console.log(rows.value[0]);
rows.value[2] = 10
console.log(rows)
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

  