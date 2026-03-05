<script setup></script>

<template>
  <header>
    <nav class="mb-4 flex gap-4">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/flowers">Flowers</RouterLink>
      <RouterLink to="/computed">Computed</RouterLink>
      <RouterLink to="/store">Store Test</RouterLink>
      <RouterLink to="/tasks">Tasks</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style>
.btn-primary {
  background-color: yellow;
}
</style>
