<template>
  <nav class="menu">
    <ul>
      <li>
        <router-link to="/">Home</router-link>
      </li>
      <li>
        <router-link to="/about">About</router-link>
      </li>
      <li>
        <router-link to="/download-cv">Download CV</router-link>
      </li>
      <li>
        <router-link to="/contact">Contact</router-link>
      </li>
    </ul>
  </nav>
</template>

<style>
.menu {
  background-color: #333;
}

.menu ul {
  display: flex;
  list-style: none;
  padding: 0;
}

.menu ul li {
  margin-right: 10px;
}

.menu ul li a {
  color: #fff;
  text-decoration: none;
  padding: 10px;
}
