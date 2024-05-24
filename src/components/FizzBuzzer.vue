<script setup lang="ts">
import { ref } from "vue";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";

defineProps<{ msg: string }>();

const count = ref(0);

const inputNum = ref(null);
const outputString = ref("FIZZ!");

const fbCheck = (event) => {
  if (inputNum.value % 3 == 0) {
    outputString.value = "FIZZ!";
  }
  if (inputNum.value % 5 == 0) {
    outputString.value = "BUZZ!";
  }

  if (inputNum.value % 15 == 0) {
    outputString.value = "FIZZBUZZ!";
  }

  console.log(inputNum.value);
};
</script>

<template>
  <div class="items-center flex flex-wrap gap-3 grow">
    <Input
      v-model="inputNum"
      class="min-w-fit w-auto grow"
      placeholder="e.g. 102"
    />
    <Button class="grow md:max-w-fit" @click="fbCheck">Check!</Button>
  </div>
  <div id="answer" class="output text-center text-6xl anim-pop-out">
    It's a
    <span class="anim-logo-gradient anim-turbo">{{ outputString }}!</span>
  </div>
</template>

<style scoped>
.anim-pop-out {
  animation: popOut 0.4s cubic-bezier(0.47, 1.64, 0.41, 0.8);
}

@keyframes popOut {
  0% {
    transform: scale(0%);
  }

  100% {
    transform: scale(100%);
  }
}
</style>
