<template>
  <v-container fluid class="ma-0 pa-0 emailVerified">
    <div class="emailVerified__container">
      <nav>
        <h1>CityCore</h1>
      </nav>

      <section class="body__section">
        <div class="body__section__contnet">
          <div class="center__items">
            <h1>Email Has Been Verified Successfilly</h1>
            <p>Your email was Successfilly Verified</p>

            <img src="../assets/images/emailVerified.png" />

            <div class="button">
              <v-btn depressed class="btn">
                Continue To My Account
              </v-btn>
            </div>
          </div>
        </div>
      </section>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "notFound",

  mounted() {
    let elHtml = document.getElementsByTagName("html")[0];
    elHtml.style.overflowY = "hidden";
  },

  destroyed() {
    let elHtml = document.getElementsByTagName("html")[0];
    elHtml.style.overflowY = null;
  },
};
</script>

<style lang="scss" scoped>
@import url(../assets/stylesheets/emailVerified.css);
</style>
