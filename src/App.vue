<script setup lang="ts">
import FizzBuzzer from "./components/FizzBuzzer.vue";
</script>

<template>
  <div class="background px-10 flex flex-wrap content-center gap-10">
    <div>
      <div class="text-xl">Vinnie's fancy</div>
      <div
        class="text-5xl md:text-8xl transition-all transition-duration-[250ms] ease-out anim-logo-gradient"
      >
        FIZZBUZZER!
      </div>
      <div class="text-xl mt-10">
        Input a number.
        <div>
          If the number is a multiple of 3, you will get a
          <span class="anim-logo-gradient">FIZZ!</span>
        </div>
        <div>
          If the number is a multiple of 5, you will get a
          <span class="anim-logo-gradient">BUZZ!</span>
        </div>
        <div>
          If the number is a multiple of 15, you will get a
          <span class="anim-logo-gradient">FIZZBUZZ!!</span>
        </div>
      </div>
    </div>
    <div class="grow content-center">
      <FizzBuzzer />
    </div>
    <div class="center text-xs self-end w-full">
      ©️Vincent Leung {{ new Date().getFullYear() }}
      <br/><a class="anim-logo-gradient" href="https://github.com/meowthing/FizzBuzzWeb">GitHub</a>
    </div>
  </div>
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
