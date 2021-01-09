<template>
  <div>
    <v-row id="home" justify="center">
      <Header></Header>
    </v-row>
    <v-row id="about" justify="center">
      <About></About>
    </v-row>
    <v-row id="experience" justify="center">
      <Experience></Experience>
    </v-row>
    <v-row id="education" justify="center">
      <Education></Education>
    </v-row>
    <v-row id="skills" justify="center">
      <Skills></Skills>
    </v-row>
    <v-row id="certifications" justify="center">
      <Certifications></Certifications>
    </v-row>
    <v-row id="achievements" justify="center">
      <Achievements></Achievements>
    </v-row>
    <v-fab-transition>
      <v-btn
        v-show="fab"
        v-scroll="onScroll"
        fab
        medium
        bottom
        right
        fixed
        elevation="2"
        color="primary"
        @click="toTop"
      >
        <v-icon dark>mdi-chevron-up</v-icon>
      </v-btn>
    </v-fab-transition>
  </div>
</template>

<script>
import achievements from '~/components/achievements.vue'
export default {
  components: { achievements },
  layout: 'default',
  data: () => ({
    fab: false,
  }),
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 20
    },
    toTop() {
      this.$vuetify.goTo(0)
    },
  },
}
</script>

<style scoped>
#home {
  background-image: linear-gradient(
      rgba(255, 255, 255, 0.08),
      rgba(255, 255, 255, 0.08)
    ),
    url('/background.jpg');
  background-size: cover;
  margin-bottom: 30px;
}

#about {
  margin-top: 30px;
  margin-bottom: 30px;
}

#experience {
  margin-top: 30px;
  margin-bottom: 30px;
}

#education {
  margin-top: 30px;
  margin-bottom: 30px;
}

#skills {
  margin-top: 30px;
  margin-bottom: 30px;
}

#certifications {
  margin-top: 30px;
  margin-bottom: 30px;
}

#achievements {
  margin-top: 30px;
  margin-bottom: 30px;
}

#contact {
  margin-top: 30px;
}

@-webkit-keyframes glow {
  to {
    border-color: #ffffff;
    -webkit-box-shadow: 0 0 20px #ffffff;
    -moz-box-shadow: 0 0 20px #ffffff;
    box-shadow: 0 0 20px #ffffff;
  }
}

.glowingBorder {
  border: none;
  -webkit-animation: glow 1s infinite alternate;
  -webkit-transition: border 1s linear, box-shadow 1s linear;
  -moz-transition: border 1s linear, box-shadow 1s linear;
  transition: border 1s linear, box-shadow 1s linear;
}
</style>
