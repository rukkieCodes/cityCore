<template>
  <v-container fluid class="ma-0 pa-0 home">
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
            <h1>Your Journy To Financial Freedom</h1>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi
              quod unde tempore delectus earum temporibus ex voluptatibus saepe
              minus odit suscipit necessitatibus quis eaque, facere, consequatur
              officia cumque mollitia quibusdam.
            </p>
          </div>

          <div class="buttons">
            <v-btn depressed class="btn">
              <v-icon class="icon">mdi-google-play</v-icon>
              <div class="texts">
                <p>Get it on</p>
                <p>Google Play</p>
              </div>
            </v-btn>

            <v-btn depressed class="btn">
              <v-icon class="icon">mdi-apple</v-icon>
              <div class="texts">
                <p>Download on the</p>
                <p>App Store</p>
              </div>
            </v-btn>
          </div>
        </div>
        <div class="head__section__sides__right">
          <div class="head__section__sides__right__img">
            <img class="pic1" src="../assets/images/bg1.png" alt="" />
          </div>
        </div>
      </div>
    </section>

    <section class="offer__section">
      <div class="offer__section__content">
        <div class="left__side">
          <div class="left__side__img">
            <img class="pic2" src="../assets/images/bg2.png" alt="" />
          </div>
        </div>
        <div class="right__side">
          <div class="right__side__content">
            <div class="head">
              <h1>What we offer you at city core</h1>
            </div>
            <div class="body">
              <div v-for="offer in offers" :key="offer.id" class="body__list">
                <div class="left__side">
                  <div class="content">
                    <v-icon class="icon">{{ offer.icon }}</v-icon>
                    <p>{{ offer.icon_title }}</p>
                  </div>
                </div>

                <div class="right__side">
                  <div class="content">
                    <p v-html="offer.text"></p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="facts__section">
      <div class="fact__content">
        <div class="left__side">
          <div class="left__side__content">
            <div class="head">
              <div class="left__side">
                <h1>Our Approach</h1>
              </div>

              <div class="right__side">
                <img class="pic1" src="../assets/images/dots2.png" alt="" />
              </div>
            </div>

            <div class="body">
              <div v-for="fact in left_facts" :key="fact.id" class="body__list">
                <p v-html="fact.text"></p>
              </div>
            </div>
          </div>
        </div>
        <div class="right__side">
          <div class="left__side__content">
            <div class="head">
              <div class="left__side">
                <h1>Our Strategy</h1>
              </div>

              <div class="right__side">
                <img class="pic1" src="../assets/images/dots2.png" alt="" />
              </div>
            </div>

            <div class="body">
              <div v-for="fact in right_fact" :key="fact.id" class="body__list">
                <p v-html="fact.text"></p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="steps__section">
      <div class="steps__section__content">
        <div class="left__side">
          <div class="left__side__content">
            <div class="head">
              <h1>Begin you Journy with four simple steps</h1>
            </div>

            <div class="body">
              <div class="step__list">
                <div class="left__side">
                  <div class="number">
                    <p>1</p>
                  </div>
                </div>
                <div class="right__side">
                  <div class="text">
                    <p>
                      Create an account on City Crown using your basic
                      information..
                    </p>
                  </div>
                </div>
              </div>

              <div class="breaker">
                <div class="left__side">
                  <span></span>
                </div>
                <div class="right__side"></div>
              </div>

              <div class="step__list">
                <div class="left__side">
                  <div class="number">
                    <p>2</p>
                  </div>
                </div>
                <div class="right__side">
                  <div class="text">
                    <p>
                      Create your goal(s) with a name, amount you want to save.
                    </p>
                  </div>
                </div>
              </div>

              <div class="breaker">
                <div class="left__side">
                  <span></span>
                </div>
                <div class="right__side"></div>
              </div>

              <div class="step__list">
                <div class="left__side">
                  <div class="number">
                    <p>3</p>
                  </div>
                </div>
                <div class="right__side">
                  <div class="text">
                    <p>
                      Link your debit card to your saving goal and start saving
                      money immediatly.
                    </p>
                  </div>
                </div>
              </div>

              <div class="breaker">
                <div class="left__side">
                  <span></span>
                </div>
                <div class="right__side"></div>
              </div>

              <div class="step__list">
                <div class="left__side">
                  <div class="number">
                    <p>4</p>
                  </div>
                </div>
                <div class="right__side">
                  <div class="text">
                    <p>
                      Enjoy up to 17% interest on your savings
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <div class="foot">
              <v-btn class="btn" depressed text>
                Start Your Journy
                <v-icon right>mdi-chevron-right</v-icon>
              </v-btn>
            </div>
          </div>
        </div>
        <div class="right__side">
          <div class="right__side__contnent">
            <img src="../assets/images/phone.png" alt="" />
          </div>
        </div>
      </div>
    </section>

    <section class="learn__more__section">
      <div class="learn__more__section__content">
        <div class="left__side">
          <div class="left__side__content">
            <div class="head">
              <div class="text">
                <h1>Why Choose Us</h1>
              </div>

              <div class="img">
                <img src="../assets/images/dots2.png" alt="" />
              </div>
            </div>

            <div class="lead__text">
              <p>
                With over two years impresive and consistent track records in
                delighting custumers, you are in safe hands
              </p>
            </div>

            <div
              v-for="list in learn__lists"
              :key="list.id"
              class="learn__lists"
            >
              <div class="text">
                <h4>{{ list.title }}</h4>
                <p>{{ list.text }}</p>
              </div>
            </div>

            <div class="foot">
              <v-btn depressed text class="btn">
                Learn More
                <v-icon right>mdi-chevron-right</v-icon>
              </v-btn>
            </div>
          </div>
        </div>
        <div class="right__side">
          <div class="right__side__content">
            <img src="../assets/images/bg3.png" alt="" />
          </div>
        </div>
      </div>
    </section>

    <section class="testimony__section">
      <div class="testimony__section__content">
        <div class="head">
          <div class="text">
            <h1>Why Choose Us</h1>
          </div>

          <div class="img">
            <img src="../assets/images/dots2.png" alt="" />
          </div>
        </div>

        <div class="cards">
          <div class="card__content">
            <v-card
              v-for="tesimony in testimonies"
              :key="tesimony.id"
              class="card"
            >
              <v-card-text class="card__text">
                <div class="card__info">
                  <v-avatar class="card__info__avatar" size="70">
                    <img :src="tesimony.avatar" class="d_pic" />
                  </v-avatar>

                  <div class="texts">
                    <p>{{ tesimony.name }}</p>
                    <p>{{ tesimony.position }}</p>
                  </div>
                </div>

                <div class="lead__text">
                  <p>{{ tesimony.text }}</p>
                </div>

                <div class="rating">
                  <v-rating
                    :value="tesimony.rating"
                    small
                    color="#ffc66c"
                  ></v-rating>
                </div>
              </v-card-text>
            </v-card>
          </div>
        </div>
      </div>
    </section>

    <section class="download__section">
      <div class="download__section__content">
        <v-img
          gradient="rgba(0,0,0,0.2), rgba(0,0,0,0.4)"
          src="../assets/images/bg4.jpg"
          class="bg__img"
        >
          <div class="img_content">
            <div class="img__block">
              <div class="texts">
                <h1>Get City Core Mobile App</h1>
                <p>Start investing today</p>
              </div>

              <div class="buttons">
                <v-btn depressed class="btn">
                  <v-icon class="icon">mdi-google-play</v-icon>
                  <div class="texts">
                    <p>Get it on</p>
                    <p>Google Play</p>
                  </div>
                </v-btn>

                <v-btn depressed class="btn">
                  <v-icon class="icon">mdi-apple</v-icon>
                  <div class="texts">
                    <p>Download on the</p>
                    <p>App Store</p>
                  </div>
                </v-btn>
              </div>
            </div>
          </div>
        </v-img>
      </div>
    </section>

    <footer>
      <div class="footer__content">
        <div class="grid__1">
          <div class="grid__1__content">
            <h1>citycore</h1>
            <p>
              City Core is the trademark of City Core Cooperative Investment and
              Credit Society Limited. We are backed by a team of finance experts
              with over 30 years of professional fund management experience
            </p>
          </div>
        </div>
        <div class="grid_2">
          <div class="grid__2__content">
            <div class="sub_grids">
              <div class="grid1">
                <div class="grid1__content">
                  <p>Pages</p>

                  <div class="lists">
                    <router-link class="links" to="/about">About Us</router-link>
                    <router-link class="links" to="/login">Sign In</router-link>
                    <router-link class="links" to="/signup">Create Account</router-link>
                  </div>
                </div>
              </div>
              <div class="grid2">
                <div class="grid2__content">
                  <p>Connect</p>

                  <div class="lists">
                    <p class="links">info@citicore.com.ng</p>
                    <p class="links">+234(0)9060000245</p>
                    <p class="links">+234(0)9060000245</p>
                  </div>
                </div>
              </div>

              <div class="grid3">
                <div class="grid3__content">
                  <p>Follow Us</p>

                  <div class="icons">
                    <v-btn class="btn" color="#524e4e" depressed fab x-small>
                      <v-icon class="white--text">mdi-facebook</v-icon>
                    </v-btn>
                    <v-btn class="btn" color="#524e4e" depressed fab x-small>
                      <v-icon class="white--text">mdi-twitter</v-icon>
                    </v-btn>
                    <v-btn class="btn" color="#524e4e" depressed fab x-small>
                      <v-icon class="white--text">mdi-linkedin</v-icon>
                    </v-btn>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </v-container>
</template>

<script>
import $ from "jquery";
export default {
  name: "Rukkie",
  data: () => ({
    testimonies: [
      {
        avatar: require(`../assets/images/av1.png`),
        name: `Jason Smith`,
        position: `CEO Google`,
        text: `City Core pays you higher interest as regards to what any
                    other bank would pay you on any amount saved`,
        rating: 5,
      },
      {
        avatar: require(`../assets/images/av1.png`),
        name: `Jason Smith`,
        position: `CEO Google`,
        text: `City Core pays you higher interest as regards to what any
                    other bank would pay you on any amount saved`,
        rating: 5,
      },
      {
        avatar: require(`../assets/images/av1.png`),
        name: `Jason Smith`,
        position: `CEO Google`,
        text: `City Core pays you higher interest as regards to what any
                    other bank would pay you on any amount saved`,
        rating: 5,
      },
    ],
    learn__lists: [
      {
        title: `Easy Saving`,
        text: `Save any amount and any day you want`,
      },
      {
        title: `High Intrest Returns`,
        text: `City Core pays you higher interest as regards to what any other bank would pay you on any amount saved.`,
      },
      {
        title: `No Hidden Fees`,
        text: `Your account doesn't come with any change, no SMS fees, no withdrawal fees on savings above three months.`,
      },
      {
        title: `Trusted And Secured`,
        text: `Your account doesn't come with any change, no SMS fees, no withdrawal fees on savings above three months.`,
      },
    ],

    right_fact: [
      {
        text: `City Core Limited explors and deepends its core business of consumare and corporate finance. The company has introduced strategies aimed at attracting and increasing low cost liability base and generating quality risk asset.`,
      },
    ],

    left_facts: [
      {
        text: `We have dicoverd that that long-term survival of a service company like ours depends, to a great extent, on our ability to cultivate and maintain a loyal and dedicated clientele.`,
      },
      {
        text: `To that end, we have developed a customer oriented service system in which we recognize our clients as partenars in progress; the unique need of each client is taken into consideration in our service delivery and relationship management`,
      },
    ],
    offers: [
      {
        icon: "mdi-piggy-bank",
        icon_title: "Save",
        text: `Saving money can help you become Financially Secured. At
                      City Core, we help you crete a desired tomorrow by making
                      saving money fun, easy, and rewarding. <br />
                      Begin with as low as N100, Earn as much as 17% Per Annum`,
      },
      {
        icon: "mdi-trending-up",
        icon_title: "Invest",
        text: `We will help you achieve your goals of finantial freedom, whether it's a N50,000 or N1 billion investment. <br> With our Investment plans, we ensure you money works harder for you. Earn as much as 36% Per Annum`,
      },
      {
        icon: "mdi-square-inc-cash",
        icon_title: "loans",
        text: `Saving money can help you become Financially Secured. At
                      City Core, we help you crete a desired tomorrow by making
                      saving money fun, easy, and rewarding. <br />
                      Begin with as low as N100, Earn as much as 17% Per Annum`,
      },
    ],
  }),

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
  },
};
</script>

<style lang="scss" scoped>
@import url(../assets/stylesheets/home.css);
</style>
