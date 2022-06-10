<script lang="ts">
import { defineComponent, onMounted } from "vue";
import { Typer } from "../includes/typeout";

export default defineComponent({
  name: "IndexPage",
});
</script>

<script setup lang="ts">
onMounted(() => {
  const typer = new Typer();
  typer.set();
  typer.start(".tester", 1000);
});
</script>

<template>
  <div class="index-page">
    <h1 class="type-500">This is typing a letter every 1/2 seconds</h1>
    <h1 class="type-300">This is typing a letter every 1/3 seconds</h1>
    <h1 class="type-100">This is typing a letter every 1/10 seconds</h1>
    <h1 class="tester" style="color: cornflowerblue">
      This is typing a letter every second!
    </h1>
  </div>
</template>

<style lang="scss">
.index-page {
  display: block;
}
</style>
