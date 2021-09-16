<template>
  <div class="intro">
    <p class="greetings animate__animated animate__heartBeat">
      Hi I am Deon Achuo
    </p>
    <img class="boss" src="/man.jpeg" alt="" />
    <p class="position animate__animated animate__backInRight">
      Full-Stack Developer, Blockchain Engineer and Mentor😊
    </p>
  </div>
</template>

<script scoped>
export default {};
</script>

<style>
.intro {
  display: grid;
  place-items: center;
}

.greetings {
  font-family: "Russo One";
  font-weight: Bold;
  font-size: 50px;
}
.position {
  margin-top: 20px;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
.anim {
  position: absolute;
  top: 20px;
  left: 0;
  width: 100%;
  height: 50%;
}
.boss {
  border-radius: 100px;
  width: 30%;
  z-index: 2;
}

@media screen and (max-width: 480px) {
  .greetings {
    font-size: 35px;
  }
  .position {
    margin-top: 20px;
    width: 80%;
    font-size: 15px;
  }
  .boss {
    border-radius: 100px;
    width: 80%;
    z-index: 2;
  }
}
</style>
