<template>
  <div class="app">
    <PostFormVue @create="createPost" />
    <PostListVue v-bind:CustomPosts="posts" />
  </div>
</template>

<script>
import PostFormVue from "./Components/PostForm.vue";
import PostListVue from "./Components/PostList.vue";
export default {
  components: {
    PostFormVue,
    PostListVue,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "JavaScript 1", body: "Описание поста 1" },
        { id: 2, title: "JavaScript 2", body: "Описание поста 2" },
        { id: 3, title: "JavaScript 3", body: "Описание поста 3" },
      ],
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>
