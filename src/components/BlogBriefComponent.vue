<template>
  <div class="row generic">
    <div
      class="col-lg-4 col-md-6"
      v-for="row in this.recentPostsObj.recentPosts"
      :key="row.blogUUID"
    >
      <router-link :to="{ name: 'BlogPage', params: { uuid: row.blogUUID } }">
        <div class="blogTitle">{{row.name}}</div>
        <div class="blogContent">{{row.content}}</div>
      </router-link>

    </div>
  </div>
</template>

<script>
import recentPostsData from "../handler_files/recent_posts.json";

export default {
  name: "BlogBriefCom",
  data() {
    return {
      recentPostsObj: recentPostsData,
    };
  },
};
</script>

<style scoped>
.generic {
  margin-left: 10%;
  margin-right: 10%;
  margin-top: -20px;
  text-align: left;
}

.col-lg-4 {
  padding-left: 0px;
}

.blogTitle {
  margin-top: 20px;
  font-family: "Poppins-Medium", sans-serif;
  font-size: 0.9rem;
  color: #272727;
}

.blogContent {
  margin-top: 8px;
  font-family: "Poppins", sans-serif;
  font-size: 0.8rem;
  color: #272727;
}
</style>