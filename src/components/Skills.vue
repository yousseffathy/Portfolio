<template>
  <v-lazy
    v-model="isActive"
    :options="{
      threshold: 0.75,
    }"
    min-height="800"
    transition="fab-transition"
  >
    <v-container>
      <v-row class="mt-16 mb-16 ml-0 mr-0">
        <v-col cols="12" style="align-self: center; color: white">
          <h1 class="text-h2" style="font-family: 'Yellowtail', cursive !important;">.02 My toolbox</h1>
          <h3 class="text-justify text-h5" style="font-family: 'Lato', sans-serif !important;">
            These are some technologies that I have used during my school time,
            personal projects as well as in my internships:
          </h3>
          <v-row class="mt-6">
            <v-col
              col="6"
              sm="3"
              v-for="tech in techs"
              :key="tech.name"
              style="text-align: center"
            >
              <v-icon x-large color="white" class="ma-5">{{
                tech.icon
              }}</v-icon>
              <p class="text-h6" style="font-family: 'Lato', sans-serif !important;">{{ tech.name }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-lazy>
</template>

<script>
export default {
  name: "Skills",
  data: () => ({
    techs: [
      { name: "HTML5", icon: "mdi-language-html5" },
      { name: "CSS3", icon: "mdi-language-css3" },
      { name: "Sass", icon: "mdi-sass" },
      { name: "JavaScript", icon: "mdi-language-javascript" },
      { name: "React", icon: "mdi-react" },
      { name: "Vue", icon: "mdi-vuejs" },
      { name: "NodeJS", icon: "mdi-nodejs" },
      { name: "Git", icon: "mdi-git" },
      { name: "Github", icon: "mdi-github" },
      { name: "Rest APIs", icon: "mdi-cog-stop" },
      { name: ".Net Core", icon: "mdi-dot-net" },
      { name: "firebase", icon: "mdi-firebase" },
      { name: "AWS", icon: "mdi-aws" },
      { name: "Azure", icon: "mdi-microsoft-azure" },
      { name: "SQL", icon: "mdi-database-search" },
      { name: "Python", icon: "mdi-language-python" },
    ],
    isActive: false,
  }),
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