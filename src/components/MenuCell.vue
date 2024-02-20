<script setup>
import {ref} from "vue";

const props = defineProps({
  url: String,
  width: Number,
})

let display = ref(false);
</script>

<template>
  <div class="menu-title" v-on:mouseenter="display = true;" v-on:mouseleave="display = false;">
    <router-link class="no-link-style" :to="props.url">
      <slot/>
    </router-link>
    <div v-bind:style="{display: display && $slots.secondary() ? '' : 'none'}"
         v-bind:class="{'menu-title-secondary': display && $slots.secondary()}">
      <div></div>
      <div><slot name="secondary"/></div>
    </div>
  </div>
</template>

<style scoped>
.menu-title {
  padding-top: 0.5rem;
  position: relative;
  margin-left: 1rem;
  margin-right: 1rem;
  z-index: 1;
}
.menu-title>a {
  font-size: 1rem;
  color: white;
}
.menu-title>a:hover {
  color: whitesmoke;
}
.menu-title-secondary {
  position: absolute;
  top: 1.5rem;
  left: -0.5rem;
  width: 11rem;
  opacity: 100%;
  z-index: -1;
}
.menu-title-secondary>div:first-child {
  height: 2rem;
}
.menu-title-secondary>div:last-child {
  background: darkseagreen;
  padding-left: 0.5rem;
  padding-right: 0.5rem;
  z-index: 2;
}
</style>