<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <div style="opacity: 0.0">Invisible View</div>
    <TitleDeclarationCom/>
    <BlogBriefCom/>
  </div>
</template>

<script>
// @ is an alias to /src
import TitleDeclarationCom from '../components/TitleDeclarationComponent'
import BlogBriefCom from '../components/BlogBriefComponent'

export default {
  name: 'Home',
  components: {
    TitleDeclarationCom,
    BlogBriefCom
  }
}
</script>

<style>
</style>
