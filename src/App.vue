<template>
   <div class="display-block">
      <PostForm @create="createPost"></PostForm>
      <!-- :posts - props ="posts" - Array -->
      <PostList :posts="posts"></PostList>


   </div>
</template>

<script>
import PostForm from './components/PostForm.vue'
import PostList from './components/PostList.vue'
export default {
   components: {
      PostForm, PostList
   },
   data() {
      return {
         posts: [
            { id: 1, title: "Post JS", body: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque aut dolorum error." },
            { id: 2, title: "Post VUEX", body: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque aut dolorum error." },
            { id: 3, title: "Post VUE", body: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque aut dolorum error." },
         ],
         title: '',
         body: ''
      }
   },
   methods: {
      createPost(poster, seconder, thirder) {
         // this.posts.push(post);
         console.log(poster)
         console.log(seconder)
         console.log(thirder)
      },
   }
}
</script>

<style scoped>

</style>
