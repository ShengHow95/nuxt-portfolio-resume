<template>
  <div style="width: 100%">
    <div class="text-h5 font-weight-medium text-center my-3">CONTACT ME</div>
    <div class="text-center my-3">
      <v-tooltip v-for="(contact, i) in contacts" :key="i" top>
        <template v-slot:activator="{ on, attrs }">
          <span v-bind="attrs" v-on="on">
            <v-btn
              fab
              large
              text
              :href="contact.link"
              target="_blank"
              rel="noreferrer"
            >
              <v-icon large color="white">{{ contact.icon }}</v-icon>
            </v-btn>
          </span>
        </template>
        <span>{{ contact.tooltip }}</span>
      </v-tooltip>
    </div>
    <div class="text-subtitle-2 text-center my-2">© All rights reserved.</div>
  </div>
</template>

<script>
export default {
  data: () => ({
    contacts: [
      {
        icon: '$vuetify.icons.mdiGmail',
        tooltip: 'shenghow95@gmail.com',
        link: 'mailto:shenghow95@gmail.com',
      },
      {
        icon: '$vuetify.icons.mdiLinkedin',
        tooltip: 'https://www.linkedin.com/in/sheng-how-kong/',
        link: 'https://www.linkedin.com/in/sheng-how-kong/',
      },
      {
        icon: '$vuetify.icons.mdiGithub',
        tooltip: 'https://github.com/shenghow95',
        link: 'https://github.com/shenghow95',
      },
    ],
  }),
  computed: {},
  methods: {},
}
</script>

<style scoped></style>
