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
                <h1>Welcome Back</h1>
                <p>Please Sign In to your account</p>
              </div>

              <form>
                <div class="input">
                  <input type="email" placeholder="Email Address" />
                </div>
                <div class="input">
                  <input :type="password_type" placeholder="Password" />
                  <v-icon
                    @click="take_a_peek"
                    v-if="password_type == 'password'"
                    class="icon"
                    >mdi-eye</v-icon
                  >
                  <v-icon
                    @click="done_with_pick"
                    v-if="password_type == 'text'"
                    class="icon"
                    >mdi-eye-off</v-icon
                  >
                </div>
                <div class="input">
                  <v-btn depressed class="submit">
                    Log In
                  </v-btn>
                </div>
              </form>

              <div class="foot">
                <span></span>

                <router-link class="link" to="/forgotPassword"
                  >Forgot Password</router-link
                >
                <router-link class="link" to="/signup"
                  >Don't have An Account? Create An Account</router-link
                >
              </div>
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

  data: () => ({
    password_type: "password",
  }),

  methods: {
    done_with_pick() {
      this.password_type = "password";
    },

    take_a_peek() {
      this.password_type = "text";
    },
  },

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
@import url(../assets/stylesheets/login.css);
</style>
