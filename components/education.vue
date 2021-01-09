<template>
  <v-container>
    <v-card>
      <v-card-title class="justify-center font-weight-bold">
        <v-icon large color="white">mdi-school</v-icon>
        &nbsp; EDUCATION
      </v-card-title>
      <v-card-text>
        <v-card-text>
          <v-timeline reverse :dense="$vuetify.breakpoint.smAndDown">
            <v-timeline-item
              v-for="(education, i) in educations"
              :key="i"
              :color="education.color"
              :icon="education.icon"
              fill-dot
              large
              class="mb-5"
            >
              <v-card color="#111111">
                <div class="blue darken-4 px-10">
                  <v-row class="text-h5 font-weight-medium py-4">
                    {{ education.course }}
                  </v-row>
                </div>
                <div class="px-10 py-5">
                  <v-row class="text-subtitle-1 white--text my-2">
                    {{ education.school }}
                  </v-row>
                  <v-row class="text-subtitle-1 white--text my-2">
                    {{ education.duration }}
                  </v-row>
                  <v-row class="mt-5 mb-1">
                    <v-chip
                      v-for="(stat, j) in education.status"
                      :key="j"
                      outlined
                      class="success ma-1"
                    >
                      {{ stat }}
                    </v-chip>
                  </v-row>
                </div>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    educations: [
      {
        school: 'University Sains Malaysia (USM)',
        course: 'Master of Data Science and Analytics',
        duration: 'Feb 2019 - Aug 2020',
        status: ['CGPA: 3.75'],
        icon: 'mdi-star',
        color: 'deep-purple darken-3',
      },
      {
        school: 'Curtin University Malaysia',
        course: 'Bachelor of Electrical Power Engineering',
        duration: 'Mar 2014 - Dec 2017',
        status: ['First Class Honors', 'CWA: 81.37'],
        icon: 'mdi-star',
        color: 'amber darken-3',
      },
      {
        school: 'SMK Merbau Miri (Malaysia)',
        course: 'Secondary School (SPM)',
        duration: 'Jan 2008 - Dec 2012',
        status: ['8A 1B'],
        icon: 'mdi-star',
        color: 'indigo darken-4',
      },
    ],
  }),
  methods: {},
}
</script>
