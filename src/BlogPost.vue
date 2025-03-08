<template>
    <div class="blog-post">
        <p>
            {{ message }}
        </p>
        <!--Display the id, title, and content of a blog post-->
        <h2>{{ id }} - {{ blogPostTitle }}</h2>
        <h4>{{ blogPostContent }}</h4>
        <button @click="changeBlogPostTitle">Change Blog Post Title</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'

let message = ref('This is the BlogPost component')
const props = defineProps(['id','blogPostTitle','blogPostContent']) // define in camel case 
console.log(props.blogPostTitle)
//defineProps({
  //  id: Number,
    //blogPostTitle: String,
   // blogPostContent: String
//})
function changeBlogPostTitle() {
    props.blogPostTitle = 'A Different Title'
}
</script>

<style scoped>
.blog-post {
    background-color: aqua;
    padding: 10px;
    margin-bottom: 10px;
}
</style>