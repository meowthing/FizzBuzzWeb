<script setup lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
</script>

<template>
  <div>
    <div class="text-xl">Vinnie's fancy</div>
    <div class="text-6xl anim-logo-gradient">FIZZBUZZER</div>
    <div class="text-xl">
      Input a number.
      <div>If the number is a multiple of 3, you will get a <span class="anim-logo-gradient">FIZZ!</span></div>
      <div>If the number is a multiple of 5, you will get a <span class="anim-logo-gradient">BUZZ!</span></div>
      <div>If the number is a multiple of 15, you will get a <span class="anim-logo-gradient">FIZZBUZZ!!</span></div>
    </div>
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
