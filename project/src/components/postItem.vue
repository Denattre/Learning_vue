<template>
  <div class="post">
    <div>
      <div><strong>Название:</strong>{{ post.title}}</div>
      <div><strong>Описание:</strong>{{ post.body}}</div>
    </div>
    <div class="post__btns">
      <my-button>Удалить</my-button>
    </div>  
  </div> 
</template>

<script>

export default {

  props: {
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style>
  .post {
      padding: 15px;
      margin-top: 10px;
      border: 1px solid green;
      display: flex;
      align-items: center;
      justify-content: space-between;
  }
</style>