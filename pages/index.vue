<template>
  <div class="main">
    <section class="header">
      
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projectList: [
        {
          title: "Find a Coach",
          text:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum magnam ex quod repudiandae dolores illo totam, vel soluta at pariatur nulla cupiditate qui error eius asperiores ipsum harum eaque aliquid.",
          img: "",
        },
        {
          title: "portfolio",
          text: "my new version of this portfolio :D",
          img: "path/to/img",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  height: 95vh;
  background-image: linear-gradient(
      to right bottom,
      rgba($color-primary-light, 0.835),
      rgba($color-primary-dark, 0.801)
    ),
    url(../static/cowboypulp.jpg);
  background-size: cover;
  background-position: top;
  position: relative;
  /* clip-path works clockwise */
  /* checkout https://bennettfeely.com/clippy/ */
  -webkit-clip-path: polygon(0 0, 100% 0%, 100% 71%, 0 90%);
  clip-path: polygon(0 0, 100% 0%, 100% 71%, 0 90%);
}
</style>
