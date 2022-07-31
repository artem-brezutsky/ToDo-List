<template>
  <div class="app">
    <form>
      <input class="input" type="text" placeholder="Название">
      <input class="input" type="text" placeholder="Описание">
      <button class="btn">Создать</button>
    </form>
    <div class="post" v-for="post in posts">
      <div><strong>Название: </strong>{{ post.title }}</div>
      <div><strong>Описание: </strong>{{ post.body }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {id: 1, title: 'JavaScript 1', body: 'Описание 1'},
        {id: 2, title: 'JavaScript 2', body: 'Описание 2'},
        {id: 3, title: 'JavaScript 3', body: 'Описание 3'},
      ]
    }
  },
  methods: {
    addLike() {
      this.likes++
    },
    addDislike() {
      this.disLikes++
    },
  },
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
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}

form {
  display: flex;
  flex-direction: column;
}

.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}

.btn {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
  transition: all .15s ease-in-out;
}

.btn:hover {
  background-color: teal;
  color: white;
}
</style>