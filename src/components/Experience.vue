<template>
  <v-lazy
    v-model="isActive"
    :options="{
      threshold: 0.75,
    }"
    min-height="800"
    transition="slide-x-transition"
  >
    <v-container>
      <v-row class="mt-16 mb-16 ml-0 mr-0">
        <v-col cols="12" style="align-self: center; color: white">
          <h1 class="text-h2" style="font-family: 'Yellowtail', cursive !important;">.03 The road of my journey so far</h1>
          <v-row class="mt-16 mb-16">
            <v-col cols="12" sm="3" style="align-self: center">
              <v-img class="profile" src="../assets/spreetailLogo.png"></v-img>
            </v-col>
            <v-col cols="12" sm="9" style="align-self: center; color: white">
              <h1 class="text-h3" style="font-family: 'Yellowtail', cursive !important;">Spreetail</h1>
              <p class="text-justify text-h5" style="font-family: 'Lato', sans-serif !important;">
                I have had the pleasure to spend a summer at Spreetail as a
                full-stack engineer intern with more focus on front-end
                development. I have Worked on A react front-end environment with
                .NET Core API and SQL database. I maintained and created custom
                React components that are utilized across the company's
                projetcs. I also spent a fair amount of time working on
                optimizing API average response times by creating and updating
                stored procedures of the SQL databases. I also contributed to
                creating future plans by researching and planning new features
                to be implemented.
              </p>
            </v-col>
          </v-row>
          <v-row class="mt-16">
            <v-col cols="12" sm="9" style="align-self: center; color: white">
              <h1 class="text-h3" style="font-family: 'Yellowtail', cursive !important;">LocalAnyDay</h1>
              <p class="text-justify text-h5" style="font-family: 'Lato', sans-serif !important;">
                One of the experiences I was looking for is to be part of a
                startup, and during my first internship, I got the opportunity
                to do so. During my time at LocalAnyDay, I helped redesign and
                rebrand the website. I also worked on redesigning the
                architecture of the website to reduce the average loading time.
              </p>
            </v-col>
            <v-col cols="12" sm="3" style="align-self: center">
              <v-img class="profile" src="../assets/localanyday.png"></v-img>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-lazy>
</template>

<script>
export default {
  name: "Experience",
  data: () => ({
    isActive: false,
  }),
};
</script>

<style scoped lang="scss">
.profile {
  max-width: 300px;
  max-height: 100%;
}
.header {
  font-family: 'Yellowtail', cursive;
}
</style>