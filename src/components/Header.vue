<template>
  <header class="header">
    <b-navbar
      toggleable="lg"
      type="dark"
      variant="info"
      style="padding: 0.5rem 2rem"
    >
      <div style="width: 360px">
        <div class="float-left" style="text">
          <img
            :src="require('../assets/coffee-icon.png')"
            style="width: 30px; margin: 10px 12px 10px 10px"
          />
          <!-- <img src="../assets/coffee-icon.png" style="width: 30px; margin: 10px 12px 10px 10px"/> -->
          <!-- <img
            src="../assets/coffee_with_swift.png"
            style="height: 40px; margin: 16px 0px 0px 0px"
          /> -->
        </div>
      </div>

      <!-- <b-navbar-brand href="#">NavBar</b-navbar-brand> -->

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item to="/" exact exact-active-class="active">HOME</b-nav-item>
          <b-nav-item to="/about" exact exact-active-class="active"
            >ABOUT</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    <div class="float-left subheader">
      <div class="float-left headerIcons">
        <img
          src="../assets/github-logo.png"
          class="contactIcon"
          height="22px"
        />
        <img src="../assets/stack-logo.png" class="contactIcon" height="22px" />
        <img src="../assets/linkedin.png" class="contactIcon" height="22px" />
        <img src="../assets/mail-logo.png" class="contactIcon" height="22px" />
        <img
          src="../assets/twitter-logo.png"
          class="contactIcon"
          height="22px"
        />
      </div>

    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.bg-info {
  background-color: #087a7e !important;
}

.subheader {
  background-color: #087a7e;
  width: 100%;
  padding: 0rem 2rem;
  box-shadow: 3px 3px 3px rgba(0, 0, 0, 0.2);
}

/* customizing navigation bar gap */
.headerIcons {
  margin: 10px 10px 16px 10px;
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
  margin: 0px 10px 2 0px 12px;
  color: white;
  font-size: bold;
}


</style>