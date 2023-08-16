<template>
  <h3>Список пользователей</h3>
  <PostItemVue v-for="post in CustomPosts" v-bind:key="post.id" :post="post" />
</template>

<script>
import PostItemVue from "./PostItem.vue";
export default {
  components: { PostItemVue },
  props: {
    CustomPosts: {
      type: Array,
      requaired: true,
    },
  },
};
</script>

<style scoped></style>
