<template>
  <div id="app">
    <post-form></post-form>
    <h1>{{postsCount}}</h1>
    <div class="post" v-for="post in validPosts" :key="post.id">
      <h2>{{post.title}}</h2>
      <p>{{post.body}}</p>
    </div>
  </div>
</template>

<script>
import {mapGetters, mapActions} from 'vuex'
import postForm from './components/postForm.vue'
export default {
  name: 'App',
  // computed: {
  //   allPosts(){
  //     return this.$store.getters.allPosts;
  //   }
  // }
  components: {
    postForm,
  },
  computed: mapGetters(['validPosts', 'postsCount']),
  methods: mapActions(['fetchPosts']),
  async mounted() {
    this.fetchPosts();
  }
}
</script>

<style>
#app {
  width: 400px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px auto;
}

.post {
  padding: 20px;
  border: 1px solid #111;
  border-radius: 5px;
}
</style>
