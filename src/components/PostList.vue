<template>
   <TransitionGroup name="list" tag="ol" class="list-group list-group">
      <li v-for="post in posts" :key="post.id" class="list-group-item">
         <h4>Название: {{ post.title }}</h4>
         <div class="d-flex justify-content-between align-items-cente">
            <p><strong>Описание:</strong> {{ post.body }}</p>
            <div>
               <button type="submit" class="btn btn-primary">Delete</button>
            </div>
         </div>
      </li>
   </TransitionGroup>
</template>

<script>
export default {
   props: {
      posts: {
         type: Array,
         required: true
      }
   },
   data() {
      return {

      }
   },
   methods: {

   },
   computed: {

   },
}
</script>

<style lang="scss" scoped>
.list-enter-active,
.list-leave-active {
   transition: all 0.5s ease;
}

.list-enter-from,
.list-leave-to {
   opacity: 0;
   transform: translateX(30px);
}
</style>