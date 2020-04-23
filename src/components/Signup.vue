<template>
  <v-container fluid class="ma-0 pa-0 signup">
    <div class="login__container">
      <nav>
        <h1>CityCore</h1>
      </nav>

      <section class="body__section">
        <div class="body__section__contnet">
          <div class="mobile__right__side">
            <v-img src="../assets/images/bg6.png"></v-img>
          </div>

          <div class="left__side">
            <div class="left__side__content">
              <div class="lead__text">
                <h1>Create An Account</h1>
                <p>It's super fast and easy!</p>
              </div>

              <form>
                <div class="short__inputs">
                  <div class="input">
                    <input type="text" placeholder="First Name" />
                  </div>
                  <div class="input">
                    <input type="text" placeholder="Last Name" />
                  </div>
                  <div class="input">
                    <input type="email" placeholder="Email Address" />
                  </div>
                  <div class="input">
                    <input type="text" placeholder="Phone Number" />
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
                    <input
                      :type="confirm_password_type"
                      placeholder="Confirm Password"
                    />
                    <v-icon
                      @click="take_a_peek_conf"
                      v-if="confirm_password_type == 'password'"
                      class="icon"
                      >mdi-eye</v-icon
                    >
                    <v-icon
                      @click="done_with_pick_conf"
                      v-if="confirm_password_type == 'text'"
                      class="icon"
                      >mdi-eye-off</v-icon
                    >
                  </div>
                </div>

                <div class="long__inputs">
                  <div class="input">
                    <input type="text" placeholder="Referral Code (Optional)" />
                  </div>
                  <div class="input">
                    <v-btn depressed class="submit">
                      Create Account
                    </v-btn>
                  </div>
                </div>
              </form>
            </div>
          </div>

          <div class="right__side">
            <img src="../assets/images/bg6.png" />
          </div>
        </div>
      </section>

      <!-- <section class="body__section">
        <div class="body__section__contnet">
          <div class="mobile__right__side">
            <v-img src="../assets/images/bg1.png"></v-img>
          </div>

          <div class="left__side">
            <div class="left__side__content">
              <div class="lead__text">
                <h1>Create An Account</h1>
                <p>It's super fast and easy!</p>
              </div>

              <form>
                <div class="input">
                  <input type="email" placeholder="Email Address" />
                </div>
                <div class="input">
                  <input :type="password_type" placeholder="Password" />
                  <v-icon @click="take_a_peek" v-if="password_type == 'password'" class="icon">mdi-eye</v-icon>
                  <v-icon @click="done_with_pick" v-if="password_type == 'text'" class="icon">mdi-eye-off</v-icon>
                </div>
                <div class="input">
                  <v-btn depressed class="submit">
                    Sugn Up
                  </v-btn>
                </div>
              </form>

              <div class="foot">
                <span></span>
                <router-link class="link" to="/"
                  >Already have An Account? Sign In</router-link
                >
              </div>
            </div>
          </div>

          <div class="right__side">
            <img src="../assets/images/bg1.png" />
          </div>
        </div>
      </section> -->
    </div>
  </v-container>
</template>

<script>
export default {
  name: "signup",

  data: () => ({
    confirm_password_type: "password",
    password_type: "password",
  }),

  methods: {
    done_with_pick_conf() {
      this.confirm_password_type = "password";
    },

    take_a_peek_conf() {
      this.confirm_password_type = "text";
    },

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
@import url(../assets/stylesheets/signup.css);
</style>
