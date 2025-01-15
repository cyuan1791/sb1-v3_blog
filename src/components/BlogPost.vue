<script setup lang="ts">
defineProps<{
  id: number;
  title: string;
  date: string;
  author: string;
  image: string;
  summary: string;
}>();
</script>

<template>
  <div class="card mb-4">
    <img :src="image" class="card-img-top" :alt="title">
    <div class="card-body">
      <h2 class="card-title">{{ title }}</h2>
      <p class="text-muted">
        By {{ author }} on {{ new Date(date).toLocaleDateString() }}
      </p>
      <p class="card-text">{{ summary }}</p>
      <router-link :to="'/post/' + title.replace(/\s+/g, '-').replace(/[^a-zA-Z0-9-_]/g, '')" class="btn btn-primary">Read More</router-link>
    </div>
  </div>
</template>