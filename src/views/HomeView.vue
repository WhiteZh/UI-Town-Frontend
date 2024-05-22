<script setup>
import NavigationBar from "@/components/NavigationBar.vue";
import DropDown from "@/components/DropDown.vue";
</script>

<template>
    <NavigationBar/>
    <main>
        <div style="height: 5rem;"></div>
        <DropDown><template v-slot:title>ALL</template></DropDown>
        <DropDown>
          <template v-slot:title>CSS</template>
          <template v-slot:menu>
            <p>hi</p>
          </template>
        </DropDown>
        <DropDown>
          <template v-slot:title>JavaScript</template>
          <template v-slot:menu>
            <p>hi</p>
          </template>
        </DropDown>
    </main>
</template>

<style scoped>
main {
  height: 100vh;
  max-width: 20em;
  width: 30vw;
  display: flex;
  flex-direction: column;
  padding-left: 2rem;
}



</style>
