<template>
    <div>
      <h2>Posts</h2>
      <ul class="post-list">
        <li v-for="(post, index) in posts" :key="index">
          <h3>{{ post.title }}</h3>
          <p>{{ post.description }}</p>
          <p>{{ post.content }}</p>
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const posts = ref([
    {
      title: 'Post 1',
      description: 'Description for Post 1',
      content: 'Content for Post 1',
    },
    {
      title: 'Post 2',
      description: 'Description for Post 2',
      content: 'Content for Post 2',
    },
    {
      title: 'Post 3',
      description: 'Description for Post 3',
      content: 'Content for Post 3',
    }
  ])
  </script>
  
  <style>
  .post-list {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
    margin: 0;
  }
  
  .post-list li {
    width: calc(100% / 3);
    box-sizing: border-box;
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
  }
  </style>