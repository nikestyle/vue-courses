<template>
   <form class="mb-4" @submit.prevent>
      <h3 class="mb-3">Создание поста:</h3>
      <div class="mb-3">
         <label for="exampleInputEmail1" class="form-label">Название</label>
         <input v-model="post.title" type="text" class="form-control" id="exampleInputEmail1"
            aria-describedby="emailHelp">
      </div>
      <div class="mb-3">
         <label for="exampleInputPassword1" class="form-label">Описание</label>
         <input v-model="post.body" type="text" class="form-control" id="exampleInputPassword1">
      </div>
      <button @click="createPost" type="submit" class="btn btn-primary">Submit</button>
   </form>
</template>

<script>
export default {
   data() {
      return {
         post: {
            title: '',
            body: ''
         }
      }
   },
   methods: {
      createPost() {
         this.post.id = Date.now();
         this.$emit('create', this.post, 'second', 'third')
         this.post = {
            title: '',
            body: ''
         }
      }
   },
   computed: {

   },
}
</script>

<style lang="scss" scoped>

</style>