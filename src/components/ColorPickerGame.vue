<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
// import { ref, reactive } from "@vue/reactivity";
import ColorLogic from "../composables/PickerLogic"

export default {
  setup() {
    const Mycolors = ["green", "red", "blue", "purple"];
    const { colors, message, matchColor }=ColorLogic(Mycolors);
    return {
      colors,
      message,
      matchColor
    }
  }
};
</script>

<style></style>
