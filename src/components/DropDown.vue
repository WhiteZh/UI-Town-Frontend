<script setup>

</script>

<template>
  <div class="drop-down-container">
    <div class="drop-down-btn">
      <slot name="title"/>
    </div>
    <div class="drop-down-menu"><slot name="menu"/></div>
  </div>
</template>

<style scoped>
.drop-down-container {
  position: relative;
}

.drop-down-btn {
  padding: 0.5rem 1rem;
  margin: 0;
  width: 8rem;
  display: inline-block;
  cursor: pointer;
  font-size: 1.4rem;
  font-weight: bold;
  color: white;
  text-align: left;
}

.drop-down-btn:hover {
  background-color: #272030;
  border-radius: 2rem
}

.drop-down-container:hover .drop-down-menu {
  display: inline-block;
}

.drop-down-menu {
  position: absolute;
  max-width: 10rem;
  color: white;
  display: none;
}
</style>