<template>
  <div class="app">
    <div class="nav">
      <router-link to="/">Spacer</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;500;600&display=swap");
* {
  box-sizing: border-box;
}
body {
  font-family: "Oswald", sans-serif;
  margin: 0;
  padding: 0;
}
</style>
