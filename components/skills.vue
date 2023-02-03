<template>
  <v-container>
    <v-card>
      <v-card-title class="justify-center font-weight-bold">
        <v-icon large color="white">$vuetify.icons.mdiShape</v-icon>
        &nbsp; SKILLS
      </v-card-title>
      <v-card-text>
        <template v-for="n in skillsLength">
          <v-row :key="n" class="py-2">
            <v-col v-for="i in 2" :key="i" cols="12" sm="6">
              <div
                v-if="(n - 1) * 2 + i - 1 < skills.length"
                class="text-subtitle-1"
              >
                {{ skills[(n - 1) * 2 + i - 1].name }}
              </div>
              <v-progress-linear
                v-model="skills[(n - 1) * 2 + i - 1].percent"
                color="indigo accent-4"
                height="20"
                class="rounded-pill font-weight-medium mt-2"
              >
                {{ skills[(n - 1) * 2 + i - 1].percent }}%
              </v-progress-linear>
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
    skills: [
      { name: 'Python', percent: 80 },
      { name: 'AWS Cloud', percent: 80 },
      { name: 'Git', percent: 80 },
      { name: 'SQL (PostgreSQL)', percent: 60 },
      { name: 'NoSQL (DynamoDB, Neptune)', percent: 60 },
      { name: 'Docker', percent: 60 },
      { name: 'AI/ML', percent: 40 },
      { name: 'gRPC', percent: 40 },
    ],
  }),
  computed: {
    skillsLength() {
      return Math.ceil(this.skills.length / 2)
    },
  },
  methods: {},
}
</script>
