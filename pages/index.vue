<script setup>
const { $hello } = useNuxtApp()
</script>

<template>
  <h1>Main Page</h1>
  <h2>{{ $hello('World') }}</h2>
</template>
