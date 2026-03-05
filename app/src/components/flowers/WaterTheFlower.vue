<script setup>
defineEmits(["water"])
</script>

<template>
  <button
    type="button"
    class="me-2 mb-2 rounded-lg bg-gradient-to-r from-green-400 via-green-500 to-green-600 px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-gradient-to-br focus:ring-4 focus:ring-green-300 focus:outline-none dark:focus:ring-green-800"
    @click="$emit('water')"
    @mouseover="$emit('water')"
  >
    Water
  </button>
</template>
