<template>
  <!-- <BlogPost 
  id="1" 
  blogPostTitle="What is a muggle?" 
  blogPostContent="A muggle is a person who lacks any sort of magical ability..."
  ></BlogPost>
  <BlogPost 
  id="1" 
  blog-post-title="What is a muggle?" 
  blog-post-content="A muggle is a person who lacks any sort of magical ability..."
  ></BlogPost>
  <hr />
  <BlogPost 
  :id="blogPostId" 
  :blog-post-title="blogPostTitle" 
  :blog-post-content="blogPostContent"
  ></BlogPost>

  <hr />

  <BlogPost v-for="post in posts" 
  :key="post.id"
  :id="post.id" 
  :blog-post-title="post.title" 
  :blog-post-content="post.blogPostContent"
  ></BlogPost> -->

  <div style="background-color: orange; padding: 5px;">
    <p>This is tha App Componenet</p>
    <h2>{{ blogPostId }} - {{ blogPostTitle }}</h2>
    <h4>{{ blogPostContent }}</h4>
    <button @click="blogPostTitle = 'A Different Title'">Change Blog Post Title</button>
    <BlogPost v-for="post in posts" 
    :key="post.id"
    v-bind="post"
    ></BlogPost>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import BlogPost from './BlogPost.vue'

let blogPostId = ref(2)
let blogPostTitle = ref('HP and the cursed child Broadway Production suspended until April') 
let blogPostContent = ref('Adding to the earlier post, the Broadway production oh HP...')

let posts = ref([
  {
    id: 1,
    blogPostTitle: 'What is a muggle in HP world?',
    blogPostContent: 'A muggle is a person who lacks any sort of magical ability...'
  },
  {
    id: 2,
    blogPostTitle: 'HP and the cursed child Broadway Production suspended until April',
    blogPostContent: 'Adding to the earlier post, the Broadway production oh HP...'
  },
  {
    id: 3,
    blogPostTitle: 'Potter DIY: How to make your own "Harry Potter wand"',
    blogPostContent: 'We all remember those iconic Youtube videos of people making their own wands...'
  },
  {
    id: 4,
    blogPostTitle: 'Fan project brings life to "Harry Potter" series',
    blogPostContent: 'Fanfiction is a great way to keep the Harry Potter world alive...'
  }

  
])
</script>

<style scoped>

</style>