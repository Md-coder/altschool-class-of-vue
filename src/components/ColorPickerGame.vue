<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { useColors } from '../composables/colorPicker';

export default {
  setup() {
    const componentColors = ['green', 'red', 'blue', 'purple'];
    const { colors, message, matchColor } = useColors(componentColors);
    return { colors, message, matchColor };
  },
};
</script>

<style></style>
