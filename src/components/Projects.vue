<template>
  <v-lazy
    v-model="isActive"
    :options="{
      threshold: 0.75,
    }"
    min-height="800"
    transition="slide-x-reverse-transition"
  >
    <v-container>
      <v-row class="mt-16 ml-0 mr-0">
        <v-col cols="12" style="align-self: center; color: white">
          <h1
            class="text-h2 mb-12"
            style="font-family: 'Yellowtail', cursive !important"
          >
            .04 Projects I am proud of
          </h1>
          <v-row>
            <v-col cols="12" md="6">
              <v-card dark dense shaped class="rounded-card mx-auto">
                <v-img
                  src="../assets/show.jpeg"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="250"
                  contain
                >
                </v-img>
                <v-card-title
                  class="text-h4"
                  style="font-family: 'Lato', sans-serif !important"
                  >Painless Prep</v-card-title
                >
                <v-card-text
                  class="subtitle-1"
                  style="font-family: 'Lato', sans-serif !important"
                >
                  For my first Senior Design project, I was happy to be part of
                  something new. Painless Prep is a startup that helps DIY
                  painters by providing custom window coverings. My part was to
                  create an APP that can measure the dimensions of windows
                  through an image. I have utilized OpenCV to create an
                  algorithm that does just that with an accuracy of up to 99.7%.
                  The algorithm was written in python and deployed on an EC2
                  instance.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" md="6">
              <v-card dark dense shaped class="rounded-card mx-auto">
                <v-img
                  src="../assets/cfood.jpg"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="250"
                  contain
                >
                </v-img>
                <v-card-title
                  class="text-h4"
                  style="font-family: 'Lato', sans-serif !important"
                  >Cfood</v-card-title
                >
                <v-card-text
                  class="subtitle-1"
                  style="font-family: 'Lato', sans-serif !important"
                >
                  For my second Senior Design project, I was the lead developer
                  of a team of 6 software engineers. We developed a calorie
                  tracking app using React Native. We also designed and
                  implemented a REST API using ExpressJS, which was deployed on
                  an EC2 instance to connect the app to the MySQL database
                  deployed on an RDS instance. For user management and
                  authentication, we used Google Firebase. The app was published
                  on Google Playstore.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" md="6">
              <v-card dark dense shaped class="rounded-card mx-auto">
                <v-img
                  src="../assets/vacation.png"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="250"
                  contain
                >
                </v-img>
                <v-card-title
                  class="text-h4"
                  style="font-family: 'Lato', sans-serif !important"
                  >Vacation Planner</v-card-title
                >
                <v-card-text
                  class="subtitle-1"
                  style="font-family: 'Lato', sans-serif !important"
                >
                  I believe in a hands-on approach when it comes to learning
                  something new. This project was part of my learning process of
                  designing and implementing a .NET Core from scratch with Vue.
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    icon
                    href="https://github.com/yousseffathy/VacationPlanner"
                    target="_blank"
                  >
                    <v-icon>mdi-github</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="6">
              <v-card dark dense shaped class="rounded-card mx-auto">
                <v-img
                  src="../assets/stocks.png"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="250"
                  contain
                >
                </v-img>
                <v-card-title
                  class="text-h4"
                  style="font-family: 'Lato', sans-serif !important"
                  >Stock Market Predictor</v-card-title
                >
                <v-card-text
                  class="subtitle-1"
                  style="font-family: 'Lato', sans-serif !important"
                >
                  For a Machine learning class project, I have designed an
                  algorithm that integrated both linear regression and KNN
                  regression to predict the stock market value of a company
                  given last years' trends.
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    icon
                    href="https://github.com/yousseffathy/Stock-Market-Predictor"
                    target="_blank"
                  >
                    <v-icon>mdi-github</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="6">
              <v-card dark dense shaped class="rounded-card mx-auto">
                <v-img
                  src="../assets/drone.png"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="250"
                  contain
                >
                </v-img>
                <v-card-title
                  class="text-h4"
                  style="font-family: 'Lato', sans-serif !important"
                  >Robotics</v-card-title
                >
                <v-card-text
                  class="subtitle-1"
                  style="font-family: 'Lato', sans-serif !important"
                >
                  For a robotics class, I developed tracking system for drones
                  that utilizes computer vision to track objects with certain
                  colors and intercept their movement. The algorithm was tested
                  using a simulation designed in Gazebo. The algorithm was
                  successful in tracking objects moving with speed up to 12m/s.
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    icon
                    href="https://www.youtube.com/watch?v=mjukxHDEP-0"
                    target="_blank"
                  >
                    <v-icon>mdi-youtube</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="6">
              <v-card dark dense shaped class="rounded-card mx-auto">
                <v-img
                  src="../assets/openmrs.png"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="250"
                  contain
                >
                </v-img>
                <v-card-title
                  class="text-h4"
                  style="font-family: 'Lato', sans-serif !important"
                  >OpenMRS</v-card-title
                >
                <v-card-text
                  class="subtitle-1"
                  style="font-family: 'Lato', sans-serif !important"
                >
                  A project in our junior software engineer class was to
                  contribute to OpenMRS. OpenMRS is a collaborative open-source
                  project for developing software to support the delivery of
                  health care in developing countries. For that project, I
                  worked on three tickets including bug fixes, new features as
                  well as documentation.
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn icon href="https://openmrs.org/" target="_blank">
                    <v-icon>mdi-web</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-lazy>
</template>

<script>
export default {
  name: "Projects",
  data: () => ({
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
.rounded-card {
  border-radius: 24px !important;
}
</style>