<template>
    <div class="div_global">
      <div class="div_right">
        <img :src="imageUrl" alt="Image" />
      </div>
      <div class="div_left">
        <ul>
          <li v-for="item in items" :key="item.id">{{ item.text }}</li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      imageUrl: {
        type: String,
        required: true,
      },
      items: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  
  <style>
  /* Стили для компонента */
  .div_global {
    display: flex;
  }
  
  .div_right {
    flex: 1;
  }
  
  .div_left {
    flex: 1;
  }
  </style>
  