<template>
  <div class="index-body">
    <div class="about">
      <h2>Daniel Dazarola</h2>
      <div class="about--text">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim et
          voluptate vitae ratione possimus tenetur ipsa cum temporibus delectus
          doloribus dolorem illo, quae porro blanditiis modi quasi? Alias, ab
          minus?
        </p>
      </div>
    </div>
    <div class="projects">
      <h4>My projects</h4>
      <ul>
        <li v-for="project in projectList" :key="project.title" class="about">
          <h3>{{ project.title }}</h3>
          <p>{{ project.text }}</p>
        </li>
      </ul>
    </div>
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

<style scoped>
.about {
  position: relative;
  top: 5vh;
  left: 50%;
  transform: translateX(-50%);
  max-width: 40rem;
  box-shadow: 0 0 2rem 1rem rgba(0, 0, 0, 0.6);
  z-index: 1rem;
  border: 0.01rem solid #3b8070;
  border-radius: 1rem;
  padding: 1rem;
  margin: 0.5rem;
  margin-left: 0;
  animation: mouseHoverReverse 1s forwards;
  list-style: none;
}
.about:hover {
  animation: mouseHover 1s forwards;
}

@keyframes mouseHover {
  0% {
    transform: translateX(-50%);
  }
  100% {
    transform: translateX(-50%) scale(1.1);
    box-shadow: 0 0 8rem 1rem rgba(0, 0, 0, 0.3);
    border: 0.1rem solid #3b8070;
  }
}
@keyframes mouseHoverReverse {
  0% {
    transform: translateX(-50%) scale(1.1);
  }
  100% {
    transform: translate(-50%);
  }
}

.projects h3 {
  color: #333;
  text-transform: uppercase;
}
.projects h4 {
  color: #3b8070;
  text-transform: uppercase;
  position: absolute;
  padding: 1rem;
  padding-top: 2rem;
  left: 50%;
  transform: translateX(-50%);
}
.projects {
  display: grid;
  grid-auto-flow: column;
  position: relative;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
  max-width: 90%;
  border: 0.1rem solid #000;
  color: #35495e;
  background-color: #000;
  box-shadow: 0 0 10rem 2px rgba(0, 0, 0, 0.9);
  padding: 1rem;
  margin: 5rem 0 0 0;
}
.projects .about {
  background: #fff;
  max-width: 30em;
  padding-bottom: 1rem;
  margin-bottom: 2rem;
}
ul {
  padding-left: 0;
  margin-top: 5rem;
}
</style>
