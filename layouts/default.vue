<template>
  <div>
    <nav class="navbar">
      <!-- change button class if i'm in that place -->
      <h1 id="header-title">Front End Developer</h1>
      <ul>
        <li>
          <nuxt-link to="/" :class="isHome ? 'button--green' : 'button--grey'">
            home
          </nuxt-link>
        </li>
        <li>
          <nuxt-link
            to="/contact"
            :class="isContact ? 'button--green' : 'button--grey'"
            >contact</nuxt-link
          >
        </li>
      </ul>
    </nav>
    <Nuxt />
  </div>
</template>
<script>
export default {
  data() {
    return {
      isHome: false,
      isContact: false,
    };
  },
  created() {
    if (this.$route.name === "contact") {
      this.isHome = false;
      this.isContact = true;
    }
    if (this.$route.name === "index") {
      this.isHome = true;
      this.isContact = false;
    }
  },
  methods: {},
  watch: {
    $route(to, from) {
      console.log(this.$route.name);
      if (this.$route.name === "index") {
        this.isHome = true;
      } else {
        this.isHome = false;
      }
      if (this.$route.name === "contact") {
        this.isContact = true;
      } else {
        this.isContact = false;
      }
    },
  },
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
.navbar {
  width: 100%;
  padding: 1rem;
  margin: auto;
  background-color: black;
}
li {
  list-style: none;
  display: inline-block;
  padding: 0.7rem;
}
#header-title {
  display: inline;
  color: azure;
  padding: 1rem 3rem;
  text-align: center;
}
.button--green {
  display: inline-block;
  border-radius: 4rem;
  border: 0.1rem solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 1rem 3rem;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4rem;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 1rem 3rem;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
