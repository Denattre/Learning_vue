<template>
<div>
  <h3>Список пользователей</h3>
  <post-item 
  v-for="post in posts"
  :post="post"
  />
</div>
</template>

<script>
import postItem from './postItem.vue'
  export default {
  components: { postItem },
    props: {
      posts: {
        type: Array,
        required: true,
      }
    }
  }
</script>

<style scoped>

</style>