<script setup lang="ts">
import { ref } from "vue";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";

// defineProps<{ msg: string }>();

// Little trick to force a re-render of the component by incrementing the 'key' value
// TODO: Could change to bind 'key' to the outputString instead...
const inputNum = ref("");
const outputHtml = ref("");

const fbCheck = () => {
  let stringBuilder = "";

  if (inputNum.value % 3 == 0) {
    stringBuilder += "FIZZ";
  }
  if (inputNum.value % 5 == 0) {
    stringBuilder += "BUZZ";
  }

  if (stringBuilder.length > 0) {
    outputHtml.value = `It's a <span class=\"anim-logo-gradient anim-turbo\">${stringBuilder}!</span>`;
  } else {
    outputHtml.value =
      "It's not a multiple of 3 or 5 🤷 <br/><br/> Try a different number!";
  }
};
</script>

<template>
  <div class="items-center flex flex-wrap gap-3 grow">
    <Input
      type="text"
      inputmode="numeric"
      pattern="[0-9]*"
      v-model="inputNum"
      class="min-w-fit w-auto grow"
      placeholder="e.g. 102"
      @keyup.enter="fbCheck"
    />
    <Button class="grow md:max-w-fit" @click="fbCheck">Check!</Button>
  </div>
  <div
    id="answer"
    class="output text-center text-4xl lg:text-6xl anim-pop-out"
    v-html="outputHtml"
    :key="outputHtml"
  ></div>
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
