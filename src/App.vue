<template>
  <div class="app">
    <form>
      <h4>Создание поста</h4>
      <input class="input" type="text" placeholder="Название">
      <input class="input" type="text" placeholder="Описание">
      <button>Создать</button>
    </form>
    <div class="post" v-for="post in posts">
      <div><strong>Название: </strong>{{post.title}}</div>
      <div><strong>Описание: </strong>{{post.body}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {id: 1, title: 'js', body: 'some text for js'},
        {id: 2, title: 'ts', body: 'some text for ts'},
        {id: 3, title: 'vue', body: 'some text for vue'},
      ]
    }
  },
  methods: {}
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}

.post {
  margin-top: 15px;
  padding: 15px;
  border: 2px solid green;
}
.input{
  width: 100%;
  border: 2px solid green;
  padding: 10px 15px;
  margin-top: 15px;
}
</style>
