<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <div style="opacity: 0">Invisible View</div>
    <TagsListCom />

    <TitleDeclarationCom />
    <BlogBriefCom />
  </div>
</template>

<script>
// @ is an alias to /src
import TitleDeclarationCom from "../components/TitleDeclarationComponent";
import BlogBriefCom from "../components/BlogBriefComponent";
import TagsListCom from "../components/TagsList";

export default {
  name: "Home",
  components: {
    TitleDeclarationCom,
    BlogBriefCom,
    TagsListCom
  }
};
</script>

<style scoped>

</style>
