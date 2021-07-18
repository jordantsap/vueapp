<template>
<h1>Currencies</h1>
<div v-for="post in posts" v-bind:key="post.id">
  <div :class="{'loading': loading}">
  {{ post.title }}
  </div>
</div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      posts: [],
      loading: true,
    };
  },
  methods: {
    fetchApi() {
      axios
        .get("https://my-json-server.typicode.com/typicode/demo/posts")
        .then((response) => {
          this.posts = response.data;
          this.loading = false;
          console.log(response.data[0].title);
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
  beforeMount() {
    this.fetchApi();
  },
};
</script>
