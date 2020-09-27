<template>
  <div class="row generic">
    <div
      class="col-lg-4 col-md-6"
      v-for="row in this.reversedMessage"
      :key="row.blogUUID"
    >
      <router-link :to="{ name: 'BlogPage', params: { uuid: row.blogUUID } }">
        <div class="blogTitle">{{ row.name }}</div>

        <div v-for="tagRow in row.tagsList" :key="tagRow.tagUUID">
          <b-button :style="'background-color:' + tagRow.backgroundColor + ';'" class="tagColor">{{
            tagRow.tagName
          }}</b-button>
        </div>

        <div class="blogContent">{{ row.content }}</div>
      </router-link>
    </div>
  </div>
</template>

<script>
import recentPostsData from "../handler_files/Recent_posts.json";
import tagsInfo from "../handler_files/Tags_info.json";

export default {
  name: "BlogBriefCom",
  data() {
    return {
      recentPostsObj: [],
      tagsInfoObj: tagsInfo,
    };
  },
  computed: {
    // a computed getter
    reversedMessage: function () {
      // `this` points to the vm instance
      var arrayOfPosts = recentPostsData.recentPosts;
      var arrayOfTags = tagsInfo.tagsInfoList;
      for (let i = 0; i < arrayOfPosts.length; i++) {

        var postTags = arrayOfPosts[i].tagsList;
        for (let j = 0; j < postTags.length; j++) {
          console.log(postTags[j])
          var result = arrayOfTags.filter((obj) => {
            // console.log(obj)
            return obj.tagUUID === postTags[j];
          });
          arrayOfPosts[i].tagsList = result;
        }
      }
      console.log(arrayOfPosts);
      return arrayOfPosts;
    },
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
  font-size: 1rem;
  color: #272727;
}

.blogContent {
  margin-top: 8px;
  font-family: "Roboto", sans-serif;
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