<template>
  <v-container fluid class="ma-0 pa-0 login">
    <div class="login__container">
      <nav>
        <h1>CityCore</h1>
      </nav>

      <section class="body__section">
        <div class="body__section__contnet">
          <div class="mobile__right__side">
            <v-img src="../assets/images/bg5.png"></v-img>
          </div>

          <div class="left__side">
            <div class="left__side__content">
              <div class="lead__text">
                <h1>Change Password</h1>
                <p>Please Enter Your New Password For You Account</p>
              </div>

              <form>
                <div class="input">
                  <input type="password" placeholder="Password" />
                </div>
                <div class="input">
                  <input type="password" placeholder="Password" />
                </div>
                <div class="input">
                  <v-btn depressed class="submit">
                    Reset Password
                  </v-btn>
                </div>
              </form>
            </div>
          </div>

          <div class="right__side">
            <img src="../assets/images/bg5.png" />
          </div>
        </div>
      </section>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "home",

  mounted() {
    let elHtml = document.getElementsByTagName("html")[0];
    elHtml.style.overflowY = "hidden";
  },

  destroyed() {
    let elHtml = document.getElementsByTagName("html")[0];
    elHtml.style.overflowY = null;
  }
};
</script>

<style lang="scss" scoped>
@import url(../assets/stylesheets/login.css);
</style>
