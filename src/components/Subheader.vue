<template>
    <div class="float-left subheader">
       <div class="float-left headerIcons">
         <img src="../assets/github-logo.png" class="contactIcon" height="22px" />
          <img src="../assets/stack-logo.png" class="contactIcon" height="22px" />
          <img src="../assets/linkedin.png" class="contactIcon" height="22px" />
          <img src="../assets/mail-logo.png" class="contactIcon" height="22px" />
          <img src="../assets/twitter-logo.png" class="contactIcon" height="22px"/>
       </div>
        <!-- <div class="float-left header_title">Weekly iOS, Swift, SwiftUI & Xcode Posts & Tips</div> -->
    </div>
</template>

<script>
export default {
    name: "subheader"
}
</script>

<style scoped>

.subheader {
    background-color: #087A7E;
    width: 100%;
    padding: 0.0rem 2rem;
}

/* customizing navigation bar gap */
.headerIcons {
  margin: 10px 10px 20px 10px; 
  width: 100%; 
  text-align: left;
}
.contactIcon {
    margin-bottom: 8px;
    margin-left: 4px;
    margin-right: 8px;
}

.header_title {
    
    text-align: left; 
    margin: 0px 10px 2  0px 12px;
    color: white;
    font-size: bold;
}

</style>