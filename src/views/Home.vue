<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <div style="opacity: 0.0">Invisible View</div>

    <div class="row tags">
      <div v-for="row in this.tagsInfoObj.tagsInfoList"
      :key="row.tagUUID">

      <b-button :style="'background-color: ' + row.backgroundColor + '; margin-left: 10px'" 
      class="float-left tagColor">{{row.tagName}}</b-button>
      
      </div>
      
      <!-- <b-button style="background-color: #222831;" 
      class="float-left tagColor">News</b-button>
      <b-button style="background-color: #0085ba; margin-left: 10px;" 
      class="float-left tagColor">SwiftUI</b-button>
      <b-button style="background-color: #ff4b5c; margin-left: 10px;" 
      class="float-left tagColor">Swift</b-button>
      <b-button style="background-color: #81b214; margin-left: 10px;" 
      class="float-left tagColor">UIKit</b-button>
      <b-button style="background-color: #557571; margin-left: 10px;" 
      class="float-left tagColor">Xcode</b-button>
      <b-button style="background-color: #ba6b57; margin-left: 10px;" 
      class="float-left tagColor">Tips</b-button>
      <b-button style="background-color: #776d8a; margin-left: 10px;" 
      class="float-left tagColor">Data Structure</b-button> -->
    </div>

    <TitleDeclarationCom/>
    <BlogBriefCom/>
  </div>
</template>

<script>
// @ is an alias to /src
import TitleDeclarationCom from '../components/TitleDeclarationComponent'
import BlogBriefCom from '../components/BlogBriefComponent'

import tagsInfo from '../handler_files/Tags_info.json'

export default {
  name: 'Home',
  components: {
    TitleDeclarationCom,
    BlogBriefCom
  },
  data() {
    return {
      tagsInfoObj: tagsInfo
    }
  }
}
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
</style>
