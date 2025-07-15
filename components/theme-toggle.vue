<script lang ="ts" setup>
import { computed } from "vue";

const colorMode = useColorMode();

const isDark = computed({
  get() {
    return colorMode.value === "dark";
  },
  set(value: boolean) {
    colorMode.preference = value ? "dark" : "light";
  },
});
</script>

<template>
  <label class="swap swap-rotate">
    <!-- this hidden checkbox controls the state -->
    <input v-model="isDark" type="checkbox">

    <Icon
      name="hugeicons:sun-03"
      size="24"
      class="swap-on"
    />

    <!-- moon icon -->
    <Icon
      name="hugeicons:moon-01"
      class="swap-off"
      :size="24"
    />
  </label>
</template>
