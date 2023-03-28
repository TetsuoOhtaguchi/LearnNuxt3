<script setup>
// $fetch関数
// const posts = ref([])
// const data = await $fetch('https://jsonplaceholder.typicode.com/posts/')
// posts.value = data

const data = await $fetch('/api/user', {
  method: 'POST',
  body: { name: 'John Doe' }
})
console.log(data)

// fetch関数
// const posts = ref([])
// const response = await fetch('https://jsonplaceholder.typicode.com/posts/')
// const data = await response.json()
// posts.value = data

const response = await fetch('/api/user', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({ name: 'John Doe' })
})
console.log(response)
</script>

<template>
  <div>
    <h1>Posts一覧</h1>
    <!-- <p v-if="error">{{ error }}</p>
    <ul>
      <li v-for="post in posts" :key="post.id">{{ post.title }}</li>
    </ul> -->
  </div>
</template>
