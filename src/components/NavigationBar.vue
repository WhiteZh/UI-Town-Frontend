<script setup>
import MenuCell from "@/components/MenuCell.vue";
</script>

<template>
  <nav class="navbar">
    <a class="home-title no-link-style" href="/">UI Town</a>
    <MenuCell url="/">About Us</MenuCell>
    <MenuCell url="/">
      CSS
      <template v-slot:secondary>
        <div style="margin: 0 1rem 0 1rem;">hwllo</div>
      </template>
    </MenuCell>
    <MenuCell url="/">JavaScript</MenuCell>
  </nav>
</template>

<style scoped>
.navbar {
  height: 5em;
  background: darkseagreen;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0 1rem 0 1rem;
}

.home-title {
  font-size: 2rem;
  color: white;
  padding: 0 1.5rem 0 0.5rem;
  margin-right: 1rem;
}
.home-title:hover {
  color: whitesmoke;
}
</style>