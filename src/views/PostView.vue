<script setup lang="ts">
import { computed } from 'vue';
import { useRoute } from 'vue-router';
import posts from '../data/posts.json';

const route = useRoute();
const post = computed(() => {
  return posts.posts.find(p => p.id === Number(route.params.id));
});
</script>

<template>
  <div class="container mt-4" v-if="post">
    <div class="row">
      <div class="col-md-8">
        <img :src="post.image" class="img-fluid mb-4" :alt="post.title">
        <h1>{{ post.title }}</h1>
        <p class="text-muted">
          By {{ post.author }} on {{ new Date(post.date).toLocaleDateString() }}
        </p>
        <div class="content mt-4">
          {{ post.content }}
        </div>
        <router-link to="/" class="btn btn-secondary mt-4">Back to Posts</router-link>
      </div>
    </div>
  </div>
</template>