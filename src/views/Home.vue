<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <div style="opacity: 0">Invisible View</div>

    <!-- Tags List -->
    <div class="row tags">
      <div
        v-for="(row, index) in this.tagsInfoObj.tagsInfoList"
        :key="row.tagUUID"
      >

        <div :style="index == 0 ? 'margin-left: 0px;' : 'margin-left: 10px;'">
          <b-button
            :style="'background-color:' + row.backgroundColor + ';'"
            class="float-left tagColor"
            >{{ row.tagName }}</b-button>
        </div>
      </div>

      <!-- 
        <b-button style="background-color: #222831;" 
      class="float-left tagColor">News</b-button>
      -->
    </div>

    <TitleDeclarationCom />
    <BlogBriefCom />
  </div>
</template>

<script>
// @ is an alias to /src
import TitleDeclarationCom from "../components/TitleDeclarationComponent";
import BlogBriefCom from "../components/BlogBriefComponent";

import tagsInfo from "../handler_files/Tags_info.json";

export default {
  name: "Home",
  components: {
    TitleDeclarationCom,
    BlogBriefCom,
  },
  data() {
    return {
      tagsInfoObj: tagsInfo,
    };
  },
};
</script>

<style scoped>
.tags {
  margin-left: 10%;
  margin-right: 10%;
  width: 100%;
  /* margin-top: 80px; */
  text-align: left;
}

.tagColor {
  background-color: #d2f6c5;
  color: white;
  align-content: left;
  text-align: left;

  font-family: "Roboto-bold", sans-serif;
  font-size: 0.8rem;
  padding-top: 4px;
  padding-bottom: 4px;
  border-radius: 6px;
  border-width: 0px;
  margin-bottom: 50px;
}

.tagLeftMargin {
  margin-left: 10px;
}
</style>
