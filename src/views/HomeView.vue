<script setup>
  import {ref} from "vue";
  import NavigationBar from "@/components/NavigationBar.vue";
  import DropDown from "@/components/DropDown.vue";

  let CSS_attribute = ref([
    {name: 'Buttons', url: '/'},
    {name: 'Checkboxes', url: '/'},
    {name: 'Toggle Switches', url: '/'},
    {name: 'Loads', url: '/'},
    {name: 'Transitions', url:'/'},
    {name: 'Special Effects', url: '/'}
  ]);
  let JS_attribute = ref([
    {name: 'Mouse Effect', url: '/'},
    {name: 'Background', url: '/'},
    {name: 'Menu', url: '/'},
    {name: 'Visible Chart', url: '/'}
  ]);
</script>

<template>
  <NavigationBar/>
  <div class="main">
    <div class="left-nav">
        <div style="height: 10rem;"></div>
        <DropDown>All</DropDown>
        <DropDown :list="CSS_attribute">CSS</DropDown>
        <DropDown :list="JS_attribute">JavaScript</DropDown>
    </div>
    <div class="content">
      <h3>To Select</h3>
      <h6>Choose the code of your choice</h6>
    </div>
  </div>

</template>

<style scoped>
.main {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
}

.content {
  flex-grow: 1;
}

.content>h3 {
  font-size: 1.75rem;
  color: #D0C3F1;
  text-indent: 2rem;
}

.content>h6 {
  color: #D0C3F1;
  letter-spacing: 0.2rem;
  font-family: Cooljazz, sans-serif;
  font-weight: lighter;
  font-style: italic;
  text-indent: 2rem;
}

.left-nav {
  width: 20rem;
  display: flex;
  flex-direction: column;
  margin-left: 1rem;
  align-items: start;
}

@media (max-width: 61rem) {
  .left-nav {
    display: none;
  }
}


</style>
