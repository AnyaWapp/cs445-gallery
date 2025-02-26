<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="greetings">
    <h1 class="black">{{ msg }}</h1>
  </div>
</template>

<style scoped>
.header {
  text-align: center;
  padding: 20px 0; 
}

.title {
  font-size: 2rem;
  font-weight: bold;
  color: black;
}
</style>
