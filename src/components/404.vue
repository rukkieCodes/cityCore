<template>
  <v-container fluid class="ma-0 pa-0 notFount">
    <section class="head__section">
      <div class="navs">
        <div class="desktop__nav">
          <nav>
            <div class="title">
              <h1>CityCore</h1>
            </div>

            <div class="nav__middle__links">
              <v-btn text depressed class="nav__middle__link__button">
                <v-icon class="nav__middle__link__button__icon"
                  >mdi-home</v-icon
                >
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
              <v-btn to="/login" text depressed class="last__link__buttons">
                <v-icon class="nav__middle__link__button__icon"
                  >mdi-login</v-icon
                >
                Log In
              </v-btn>
              <v-btn to="/signup" text depressed class="last__link__buttons">
                <v-icon class="nav__middle__link__button__icon"
                  >mdi-account</v-icon
                >
                Create Account
              </v-btn>
            </div>
          </nav>
        </div>

        <div class="mobile__nav">
          <nav class="head">
            <v-btn
              @click="open_drawer"
              class="side__nav__toggle"
              depressed
              icon
            >
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
                  <v-icon class="nav__middle__link__button__icon"
                    >mdi-home</v-icon
                  >
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
                <v-btn to="/login" text depressed class="last__link__buttons">
                  <v-icon class="nav__middle__link__button__icon"
                    >mdi-login</v-icon
                  >
                  Log In
                </v-btn>
                <v-btn to="/signup" text depressed class="last__link__buttons">
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

      <div class="head__section__sides">
        <div class="head__section__sides__left">
          <div class="texts">
            <h1>Oop...The page you were looking for does not exit</h1>
            <p>The page you were looking for was deleted or doesn't exit</p>
          </div>

          <div class="buttons">
            <v-btn to="/" depressed class="btn">
              Back To Homepage
            </v-btn>
          </div>
        </div>
        <div class="head__section__sides__right">
          <div class="head__section__sides__right__img">
            <img class="pic1" src="../assets/images/notfound.png" alt="" />
          </div>
        </div>

        <div class="foot">
          <div class="foot__content">
            <div class="grid1">
              <div class="grid1__content">
                <p class="head">Frequently Asked Questions</p>
                <p class="text">
                  Go through our list of frequently asked questions and see if
                  you can find exactly what you are looking for
                </p>
                <v-btn class="btn" text depressed>
                  Go To FAQ Page
                  <v-icon right>mdi-chevron-right</v-icon>
                </v-btn>
              </div>
            </div>
            <div class="grid2">
              <div class="grid2__content">
                <p class="head">Contact Us</p>
                <p class="text">
                  If you have any enquiries or question and you want to quickly
                  reach to us. Kindly use the email address below
                </p>
                <v-btn class="btn" text depressed>
                  Email us at info@citycore.com.ng
                  <v-icon right>mdi-chevron-right</v-icon>
                </v-btn>
              </div>
            </div>
            <div class="grid3">
              <div class="grid3__content">
                <p class="head">Live Support Page</p>
                <p class="text">
                  Have an urgent enquiry. Our support team is live 24/7 to
                  respond to all your request. Simply click the link below
                </p>
                <v-btn class="btn" text depressed>
                  Go to Our Live Support Page
                  <v-icon right>mdi-chevron-right</v-icon>
                </v-btn>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </v-container>
</template>

<script>
import $ from "jquery";
export default {
  name: "notFound",

  methods: {
    close_drawer() {
      $(".nav__drawer").hide(100);
    },

    open_drawer() {
      $(".nav__drawer").show(100);
    },
  },

  mounted() {
    $(".nav__drawer").hide();
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
@import url(../assets/stylesheets/pageNotFound.css);
</style>
