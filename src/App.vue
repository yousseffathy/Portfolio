<template>
  <v-app>
    <v-dialog v-model="dialog" persistent max-width="600px">
      <v-card dark dense>
        <v-card-title>
          <span class="text-h5">Send Me an Email</span>
        </v-card-title>
        <v-card-text>
          <v-form ref="form" v-model="valid" lazy-validation>
            <v-text-field
              v-model="name"
              :rules="nameRules"
              label="Name*"
              required
            ></v-text-field>

            <v-text-field
              v-model="email"
              :rules="emailRules"
              label="E-mail*"
              required
            ></v-text-field>

            <v-textarea
              v-model="message"
              label="Message*"
              :rules="messageRules"
              required
              outlined
              class="mt-4"
            ></v-textarea>
            <v-row>
              <v-spacer></v-spacer>
              <v-btn
                :disabled="!valid"
                color="success"
                class="mr-4"
                @click="send"
                type="submit"
              >
                Send
              </v-btn>

              <v-btn color="error" class="mr-4" @click="reset"> Cancel </v-btn>
            </v-row>
          </v-form>
          <small>*indicates required field</small>
        </v-card-text>
      </v-card>
    </v-dialog>
    <v-app-bar
      app
      dense
      dark
      hide-on-scroll
      class="black"
      style="max-width: 100%"
    >
      <v-toolbar-title style="font-family: 'Yellowtail', cursive"> Youssef Fathy </v-toolbar-title>
      <v-spacer />
      <v-btn icon color="white" @click="dialog = true">
        <v-icon>mdi-email-edit</v-icon>
      </v-btn>
      <v-btn
        icon
        color="white"
        href="https://www.linkedin.com/in/youssef-fathy/"
        target="_blank"
      >
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>
      <v-btn
        icon
        color="white"
        href="https://github.com/yousseffathy/"
        target="_blank"
      >
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main class="main">
      <div class="parallax">
        <v-row align="center" justify="center" style="max-width: 100%">
          <v-col class="text-center text" cols="12">
            Hi, I'm <span class="highlight">Youssef Fathy</span>. <br />
            I'm a full-stack web developer.
          </v-col>
        </v-row>
      </div>
      <Intro />
      <Skills />
      <Experience />
      <Projects />
      <v-footer dark padless>
        <v-card
          flat
          tile
          class="white--text text-center"
          color="black"
          style="width: 100%"
        >
          <v-card-text>
            <v-btn class="mx-4 white--text" icon @click="dialog = true">
              <v-icon size="24px">mdi-email-edit</v-icon>
            </v-btn>
            <v-btn
              class="mx-4 white--text"
              icon
              href="https://www.linkedin.com/in/youssef-fathy/"
            >
              <v-icon size="24px">mdi-linkedin</v-icon>
            </v-btn>
            <v-btn
              class="mx-4 white--text"
              icon
              href="https://github.com/yousseffathy/"
            >
              <v-icon size="24px">mdi-github</v-icon>
            </v-btn>
          </v-card-text>

          <v-card-text class="white--text pt-0">
            Designed and coded by Youssef Fathy. Check out my github, I am
            always working on something. You can also reach out to me by email
            or on linkedin!
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text class="white--text">
            {{ new Date().getFullYear() }} — <strong>Youssef Fathy</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </v-main>
  </v-app>
</template>

<script>
import Intro from "./components/Intro";
import Skills from "./components/Skills";
import Experience from "./components/Experience";
import Projects from "./components/Projects";
import emailjs from "emailjs-com";

export default {
  name: "App",
  components: {
    Intro,
    Skills,
    Experience,
    Projects,
  },

  data: () => ({
    dialog: false,
    valid: true,
    name: "",
    nameRules: [(v) => !!v || "Name is required"],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
    ],
    message: "",
    messageRules: [(v) => !!v || "Message is required"],
  }),
  methods: {
    validate() {
      this.$refs.form.validate();
    },
    reset() {
      this.$refs.form.reset();
      this.dialog = false;
    },
    send() {
      const verify = this.$refs.form.validate();
      if (verify) {
        const form = {
          user_name: this.name,
          user_email: this.email,
          message: this.message,
        };
        emailjs
          .send(
            "service_zzmgunr",
            "template_dbpa80a",
            form,
            "user_p2ib5aUJOspXomHlUb7MV"
          )
          .then(
            (result) => {
              console.log("SUCCESS!", result.text);
            },
            (error) => {
              console.log("FAILED...", error.text);
            }
          );
        this.reset();
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Yellowtail&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Lato:ital@1&display=swap');
.main{
  background-image: url("./assets/brick3.jpg");
  background-attachment: fixed;
}
.parallax {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("./assets/rain.gif");
  height: calc(100vh + 10px);
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.text {
  color: white;
  font-size: calc(2vw + 1.5vh + 1.5vmin);
  pointer-events: none;
  z-index: 1;
  font-family: 'Lato', sans-serif;
  
}
.highlight {
  font-family: 'Yellowtail', cursive;
  text-shadow:
      0 0 7px #fff,
      0 0 10px #fff,
      0 0 21px #fff,
      0 0 42px #5271ff,
      0 0 82px #5271ff,
      0 0 92px #5271ff,
      0 0 102px #5271ff,
      0 0 151px #5271ff;
}
</style>