<template>
  <v-container>
    <v-card>
      <v-card-title class="justify-center font-weight-bold">
        <v-icon large color="white">$vuetify.icons.mdiCertificate</v-icon>
        &nbsp; CERTIFICATIONS
      </v-card-title>
      <v-card-text>
        <template v-for="n in certificationsLength">
          <v-row :key="n" class="py-2">
            <v-col
              v-for="i in 3"
              :key="i"
              cols="12"
              sm="4"
              class="text-center text-subtitle-1"
            >
              <div
                v-if="(n - 1) * 3 + i - 1 < certifications.length"
                class="d-flex justify-center my-2"
              >
                <a
                  :href="certifications[(n - 1) * 3 + i - 1].link"
                  target="_blank"
                  rel="noreferrer"
                >
                  <v-img
                    :alt="certifications[(n - 1) * 3 + i - 1].name"
                    :src="certifications[(n - 1) * 3 + i - 1].logo"
                    max-width="150"
                  ></v-img>
                </a>
              </div>
              <div
                v-if="(n - 1) * 3 + i - 1 < certifications.length"
                class="mt-5"
              >
                {{ certifications[(n - 1) * 3 + i - 1].name }}
              </div>
            </v-col>
          </v-row>
        </template>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    certifications: [
      {
        name: 'AWS Certified Cloud Practitioner',
        logo: '/aws-certified-cloud-practitioner.png',
        link:
          'https://www.youracclaim.com/badges/52e0a23c-ddf6-4f0b-b9e1-79e2695b9c0b/public_url',
      },
      {
        name: 'AWS Certified Developer – Associate',
        logo: '/aws-certified-developer-associate.png',
        link:
          'https://www.youracclaim.com/badges/c1b820c3-b20d-4d8c-82e2-f6caedfcdff9/public_url',
      },
      {
        name: 'AWS Certified Solution Architect – Associate',
        logo: '/aws-certified-solutions-architect-associate.png',
        link:
          'https://www.youracclaim.com/badges/c1b820c3-b20d-4d8c-82e2-f6caedfcdff9/public_url',
      },
      {
        name: 'AWS Certified Data Analytics – Specialty',
        logo: '/aws-certified-data-analytics-specialty.png',
        link:
          'https://www.youracclaim.com/badges/f4f52157-d945-4e24-96de-afda7781c06c/public_url',
      },
      {
        name: 'AWS Certified Machine Learning – Specialty',
        logo: '/aws-certified-machine-learning-specialty.png',
        link:
          'https://www.youracclaim.com/badges/e9f0f347-4290-4b80-9339-31e17696d05c/public_url',
      },
    ],
  }),
  computed: {
    certificationsLength() {
      return Math.ceil(this.certifications.length / 3)
    },
  },
  methods: {},
}
</script>
