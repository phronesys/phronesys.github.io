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
      <ul>
        <li v-for="project in projectList" :key="project.title" class="project"> 
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
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum magnam ex quod repudiandae dolores illo totam, vel soluta at pariatur nulla cupiditate qui error eius asperiores ipsum harum eaque aliquid.",
          img: ""
        },
        {
          title: "portfolio",
          text: "my new version of this portfolio :D",
          img: "path/to/img"
        }
      ],
    };
  },
};
</script>

<style scoped>
.about {
  position: relative;
  top: 2rem;
  left: 50%;
  transform: translateX(-50%);
  max-width: 40rem;
  box-shadow: rgba(0, 0, 0, 1);
  z-index: 1rem;
  border: 2px solid #3b8070;
  border-radius: 1rem;
  padding: 1rem;
  margin: 0.5rem;
}
.project h3{
  color: #fff;
  text-transform: uppercase;
}
.projects {
  position: relative;
  max-width: 80%;
  border: 0.1rem solid #000;
  color: #35495e;
  background-color: #000;
  top: 3rem;
  left: 50%;
  transform: translateX(-50%);
  padding: 1rem;
}
</style>
