<template>
  <div class="row generic">
    <div
      class="col-lg-4 col-md-6"
      v-for="row in this.recentPostsObj.recentPosts"
      :key="row.blogUUID"
    >
      <router-link :to="{ name: 'BlogPage', params: { uuid: row.blogUUID } }">
        <div class="blogTitle">{{row.name}}</div>
        <b-button style="background-color: #0085ba;" class="tagColor">SwiftUI</b-button>
        <div class="blogContent">{{row.content}}</div>
      </router-link>

    </div>
  </div>
</template>

<script>
import recentPostsData from "../handler_files/Recent_posts.json";

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
  font-family: "Roboto-Medium", sans-serif;
  font-size: 1.0rem;
  color: #272727;
}

.blogContent {
  margin-top: 8px;
  font-family: 'Roboto', sans-serif;
  font-size: 0.9rem;
  color: #272727;
}

.tagColor {
  background-color: #d2f6c5;
  color: white;
  align-content: left;
  text-align: left;

  font-family: "Roboto-bold", sans-serif;
  font-size: 0.65rem;
  padding-top: 4px;
  padding-bottom: 3px;
  padding-left: 8px;
  padding-right: 8px;
  border-radius: 6px;
  border-width: 0px;
  
  margin-top: 6px;
}
</style>