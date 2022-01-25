<template>
  <v-container class="mt-16 mb-16">
    <v-row class="mt-16 ml-0 mr-0 container">
      <v-col cols="12" sm="3" style="align-self: center">
        <v-img class="profile" src="../assets/me.jpg"></v-img>
      </v-col>
      <v-col cols="12" sm="9" style="align-self: center; color: white">
        <h1>.01 Who Am I</h1>
        <p class="text-justify text-h6">
          I am a full-stack developer with a passion for delivering exceptional
          digital experiences through simple but efficient UI elements. I am
          detail-oriented and always looking to develop myself to be better. I
          have a BS in Software Engineering and a minor in Mathematics from
          University of Nebraska Lincoln. Although my focus is on front-end
          development, I also know that data is beautiful. I have worked on
          multiple backend stacks as well as on machine learning projects. I am
          currently open to job opportunities. Get In Touch!
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Intro",
};
</script>

<style scoped lang="scss">
.profile {
  object-fit: cover;
  border-radius: 100%;
  max-height: 300px;
  max-width: 300px;
  aspect-ratio: 1 / 1;
  padding: 15px;
}
</style>