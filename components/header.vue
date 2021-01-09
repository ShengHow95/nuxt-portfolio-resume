<template>
  <div>
    <v-row justify="center">
      <v-img
        src="profile.webp"
        class="rounded-circle glowingBorder"
        style="margin: 75px 0 25px 0"
        max-width="200px"
      ></v-img>
    </v-row>
    <v-row
      justify="center"
      class="text-h4 white--text text-center font-weight-black ma-5"
    >
      Jeff Kong Sheng How
    </v-row>
    <v-row class="white ma-5" style="height: 1px"></v-row>
    <v-row
      justify="center"
      class="text-h5 white--text text-center font-weight-bold ma-5"
    >
      Full Stack Developer
    </v-row>
    <v-row justify="center" class="ma-10">
      <v-btn
        outlined
        color="warning"
        href="/Resume_KongShengHow_2020.12.28.pdf"
        target="_blank"
      >
        Download Resume
      </v-btn>
    </v-row>
  </div>
</template>

<script>
export default {
  methods: {},
}
</script>

<style scoped>
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
