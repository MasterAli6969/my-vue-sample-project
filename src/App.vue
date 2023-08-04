<template>
  <div id="app">
    <MyBlock :imageUrl="imageUrl" :items="listItems" />
  </div>
</template>

<script>
import MyBlock from "./components/MyBlock.vue";

export default {
  components: { MyBlock },
  data() {
    return {
      imageUrl: "https://example.com/image.jpg",
      listItems: [
        { id: 1, text: "Пункт 1" },
        { id: 2, text: "Пункт 2" },
        { id: 3, text: "Пункт 3" },
      ],
    };
  },
};
</script>
