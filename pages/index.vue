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
    <div class="project-box">
      <ul>
        <li
          v-for="project in projectList"
          :key="project.title"
          class="projects"
        >
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
  box-shadow: 0 0 2rem 1rem rgba(0, 0, 0, 1);
  z-index: 1rem;
  border: 0.3rem solid #fff;
  border-radius: 1rem;
  padding: 1rem;
  margin: 0.5rem;
  animation: mouseHoverReverse 1s forwards;
}
.about:hover {
  animation: mouseHover 1s forwards;
}

@keyframes mouseHover {
  0%{
    transform: translateX(-50%)
  }
  100% {
    transform: translateX(-50%) scale(1.1);
    box-shadow: 0 0 8rem 1rem rgba(0, 0, 0, .7);
    border: .1rem solid #3b8070;
  }
}
@keyframes mouseHoverReverse {
  0%{
    transform: translateX(-50%) scale(1.1);
  }
  100% {
    transform: translate(-50%);
  }
}
.project-box {
  
}
.projects h3 {
  color: #fff;
  text-transform: uppercase;
}
.projects {
  position: relative;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
  max-width: 80%;
  border: 0.1rem solid #000;
  color: #35495e;
  background-color: #000;
  box-shadow: 0 0 10rem 2px rgba(0, 0, 0, 0.9);
  padding: 1rem;
  margin: 10rem 0 0 0;
}
</style>
