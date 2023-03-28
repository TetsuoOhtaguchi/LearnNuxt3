<script setup>
const response = await useFetch('https://jsonplaceholder.typicode.com/posts/')
console.log(response)
</script>

<template>
  <div>
    <h1>Posts一覧</h1>
  </div>
</template>
