<script setup>
</script>

<template>
  <nav class="navbar">
    <a class="home-title no-link-style" href="/">UITOWN</a>
    <a href="#" class="no-link-style navbar-element">Information</a>
    <a href="#" class="no-link-style navbar-element">Recommendation</a>
    <span style="flex-grow: 1"></span>
    <a href="#" class="no-link-style navbar-option" style="background-color: #1ac8db">Join in the Town</a>
    <a href="#" class="no-link-style navbar-option" style="background-color: #99dfec">Create</a>

  </nav>
</template>

<style scoped>
.navbar {
  padding: 0.5rem 1rem 0 1rem;
  height: 3.6em;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.home-title {
  font-size: 3rem;
  color: white;
  margin-right: 1.5rem;
  font-family: "Zhi Mang Xing",serif;
  align-self: center;
}
.home-title:hover {
  color: whitesmoke;
}

.navbar-element {
  align-self: flex-end;
  color: white;
  font-size: 1rem;
  font-family: "Cooljazz",serif;
  font-style: italic;
  padding-bottom: 0.6rem;
  margin-right:0.6rem;
}
.navbar-element:hover {
  color: whitesmoke;
}

.navbar-option {
  align-self: center;
  margin: 0 0.5rem 0 0.5rem;
  padding: 0.5rem 1.0rem 0.5rem 1.0rem;
  border-radius: 1rem;
  color: black;
  font-weight: bold;
}
</style>