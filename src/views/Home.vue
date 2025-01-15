<script setup lang="ts">
let myWindow = window as any;
import BlogPost from '../components/BlogPost.vue';
let postData = JSON.parse(atob(myWindow.asoneData));
let posts: any = { posts: postData }

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
