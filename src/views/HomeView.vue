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
    <main>
        <div style="height: 15rem;"></div>
        <DropDown>All</DropDown>
        <DropDown :list="CSS_attribute">CSS</DropDown>
        <DropDown :list="JS_attribute">JavaScript</DropDown>
    </main>
</template>

<style scoped>
main {
  height: 100%;
  max-width: 20em;
  width: 30vw;
  display: flex;
  flex-direction: column;
  margin-left: 2rem;
  align-items: start;
}

</style>
