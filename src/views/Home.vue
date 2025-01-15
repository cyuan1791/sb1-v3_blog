<script setup lang="ts">
import BlogPost from '../components/BlogPost.vue';
import posts from '../data/posts.json';
</script>

<template>
  <div class="container mt-4">
    <h1 class="mb-4">Blog Posts</h1>
    <div class="row">
      <div class="col-md-8">
        <BlogPost
          v-for="post in posts.posts"
          :key="post.id"
          v-bind="post"
        />
      </div>
    </div>
  </div>
</template>