<template>
  <div>
    <div class="about">
      <h2>Whoami</h2>
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
      <h2>projects</h2>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum,
        magnam ex quod repudiandae dolores illo totam, vel soluta at pariatur
        nulla cupiditate qui error eius asperiores ipsum harum eaque aliquid.
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.about {
  position: relative;
  top: 2rem;
  left: 50%;
  transform:  translateX(-50%);
  max-width: 40rem;
  box-shadow: rgba(0, 0, 0, 0.8);
  border:2px solid #3b8070;
  border-radius: 1rem;
  padding: 1rem;
  margin: .5rem;
}
.projects {
  position: relative;
  top: 3rem;
}
</style>
