<script setup lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
</script>

<template>
  <div>
    <div class="text-xl">Vinnie's fancy</div>
    <div class="text-6xl anim-logo-gradient">FIZZBUZZER</div>
    <Button>This is a button</Button>
    <Input placeholder="This is an input" />
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
