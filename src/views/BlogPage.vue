<template>
    <div>
        {{blogcontent.content}}   
        <!-- {{result}}    -->
        <!-- {{process.env.VUE_APP_ENV_VARIABLE}}   -->
    </div>
</template>

<script>

import axios from "axios";
const ax = axios.create({
  // baseURL: "http://localhost:8080/",
  baseURL: "https://kiranjas.github.io/",
});

export default {
    name: "BloePage",
    data() {
        return {
            blogcontent: { content: "Loading..." },
            result: location.host
        }
    },
  mounted() {
    let url = `page/${this.$route.params.uuid}.json`;

    ax.get(url)
      .then((response) => {
        this.blogcontent = response.data;
        console.log(response.data);
      })
      .catch((err) => {
        console.log(err);
      });
  },
}
</script>

<style scoped>

</style>