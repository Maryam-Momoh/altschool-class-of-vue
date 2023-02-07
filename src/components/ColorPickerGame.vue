<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import colorPicker from "../composables/colorPicker"

export default {
  setup() {
    
    const {colors, message, matchColor} = colorPicker()
    return { message, matchColor, colors }
  },
};
</script>

<style></style>
