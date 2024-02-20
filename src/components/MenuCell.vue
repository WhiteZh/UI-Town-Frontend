<script setup>
import {ref} from "vue";

const props = defineProps({
  url: String,
  width: Number,
})

let display = ref(false);
</script>

<template>
  <router-link class="no-link-style menu-title" :to="props.url" v-on:mouseenter="display = true;" v-on:mouseleave="display = false;">
    <slot/>
    <div v-bind:style="{display: display && $slots.secondary() ? '' : 'none'}"
         v-bind:class="{'menu-title-secondary': display && $slots.secondary()}">
      <div></div>
      <div><slot name="secondary"/></div>
    </div>
  </router-link>
</template>

<style scoped>
.menu-title {
  font-size: 1rem;
  color: white;
  padding-top: 0.5rem;
  position: relative;
  margin-left: 1rem;
  margin-right: 1rem;
  z-index: 1;
}
.menu-title:hover {
  color: whitesmoke;
}
.menu-title-secondary {
  position: absolute;
  top: 0;
  left: -0.25rem;
  width: 11rem;
  opacity: 100%;
  z-index: 2;
}
.menu-title-secondary>div:first-child {
  height: 3.5rem;
}
.menu-title-secondary>div:last-child {
  background: darkseagreen;
}
</style>