<template>
  <div class="navs">
    <div class="desktop__nav">
      <nav>
        <div class="title">
          <h1>CityCore</h1>
        </div>

        <div class="nav__middle__links">
          <v-btn text depressed class="nav__middle__link__button">
            <v-icon class="nav__middle__link__button__icon">mdi-home</v-icon>
            Home
          </v-btn>
          <v-btn text depressed class="nav__middle__link__button">
            <v-icon class="nav__middle__link__button__icon"
              >mdi-search-web</v-icon
            >
            About Us
          </v-btn>
          <v-btn text depressed class="nav__middle__link__button">
            <v-icon class="nav__middle__link__button__icon"
              >mdi-server-network</v-icon
            >
            How It Works
          </v-btn>
          <v-btn text depressed class="nav__middle__link__button">
            <v-icon class="nav__middle__link__button__icon"
              >mdi-account-cash</v-icon
            >
            Loans
          </v-btn>
          <v-btn text depressed class="nav__middle__link__button">
            <v-icon class="nav__middle__link__button__icon"
              >mdi-head-question</v-icon
            >
            Faqs
          </v-btn>
        </div>

        <div class="last__links">
          <v-btn text depressed class="last__link__buttons">
            <v-icon class="nav__middle__link__button__icon">mdi-login</v-icon>
            Log In
          </v-btn>
          <v-btn text depressed class="last__link__buttons">
            <v-icon class="nav__middle__link__button__icon">mdi-account</v-icon>
            Create Account
          </v-btn>
        </div>
      </nav>
    </div>

    <div class="mobile__nav">
      <nav class="head">
        <v-btn @click="open_drawer" class="side__nav__toggle" depressed icon>
          <v-icon>mdi-menu</v-icon>
        </v-btn>
        <div class="title">
          <h1>CityCore</h1>
        </div>
      </nav>

      <div class="nav__drawer">
        <nav class="app__side__nav">
          <div class="nav__middle__links">
            <v-btn text depressed class="nav__middle__link__button">
              <v-icon class="nav__middle__link__button__icon">mdi-home</v-icon>
              Home
            </v-btn>
            <v-btn text depressed class="nav__middle__link__button">
              <v-icon class="nav__middle__link__button__icon"
                >mdi-search-web</v-icon
              >
              About Us
            </v-btn>
            <v-btn text depressed class="nav__middle__link__button">
              <v-icon class="nav__middle__link__button__icon"
                >mdi-server-network</v-icon
              >
              How It Works
            </v-btn>
            <v-btn text depressed class="nav__middle__link__button">
              <v-icon class="nav__middle__link__button__icon"
                >mdi-account-cash</v-icon
              >
              Loans
            </v-btn>
            <v-btn text depressed class="nav__middle__link__button">
              <v-icon class="nav__middle__link__button__icon"
                >mdi-head-question</v-icon
              >
              Faqs
            </v-btn>
          </div>

          <div class="last__links">
            <v-btn text depressed class="last__link__buttons">
              <v-icon class="nav__middle__link__button__icon">mdi-login</v-icon>
              Log In
            </v-btn>
            <v-btn text depressed class="last__link__buttons">
              <v-icon class="nav__middle__link__button__icon"
                >mdi-account</v-icon
              >
              Create Account
            </v-btn>
          </div>
        </nav>

        <div @click="close_drawer" class="grey__scale"></div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";
export default {
  name: "Nav",
  data: () => ({
    drawer: true,
    links: [
      { icon: "mdi-home", text: "Home", route: "/" },
      { icon: "mdi-account", text: "About Me", route: "/about" },
      { icon: "mdi-briefcase", text: "Portfolio", route: "/portfolio" },
      { icon: "mdi-wechat", text: "Contact", route: "/contact" },
      { icon: "mdi-email-open", text: "Blog", route: "/blog" },
    ],
  }),

  methods: {
    close_drawer() {
      $(".nav__drawer").hide(100);
    },

    open_drawer() {
      $(".nav__drawer").show(100);
    }
  },

  mounted() {
    $(".nav__drawer").hide();
  },
};
</script>

<style lang="scss" scoped>
@import url(../assets/stylesheets/nav.css);
</style>
