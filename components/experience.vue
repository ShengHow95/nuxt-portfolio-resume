<template>
  <v-container>
    <v-card>
      <v-card-title class="justify-center font-weight-bold">
        <v-icon large color="white">$vuetify.icons.mdiBriefcase</v-icon>
        &nbsp; EXPERIENCE
      </v-card-title>
      <v-card-text>
        <v-timeline :dense="$vuetify.breakpoint.smAndDown">
          <v-timeline-item
            v-for="(experience, i) in experiences"
            :key="i"
            :color="experience.color"
            :icon="experience.icon"
            fill-dot
            large
            class="mb-5"
          >
            <v-card color="#111111">
              <div class="indigo darken-2 px-5 py-2">
                <v-row no-gutters class="text-h5 font-weight-medium py-2">
                  {{ experience.company }}
                </v-row>
                <v-row no-gutters class="text-subtitle-1 white--text">
                  <v-col cols="12" sm="6">{{ experience.title }}</v-col>
                  <v-col cols="12" sm="6" class="text-sm-right">
                    {{ experience.duration }}
                  </v-col>
                </v-row>
              </div>
              <v-card-text>
                <v-row
                  no-gutters
                  class="text-subtitle-1 font-weight-medium mt-5"
                >
                  Job Description:
                </v-row>
                <v-row
                  v-for="(description, j) in experience.descriptions"
                  :key="j"
                  no-gutters
                  class="mt-2"
                >
                  {{ j + 1 }}. &nbsp; {{ description }}
                </v-row>
                <v-row no-gutters class="mt-5">
                  <v-chip
                    v-for="(skill, k) in experience.skills"
                    :key="k"
                    outlined
                    class="ma-1 success"
                  >
                    {{ skill }}
                  </v-chip>
                </v-row>
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        duration: 'September 2022 - Present',
        company: 'Horangi Cyber Security',
        title: 'Solutions Architect',
        descriptions: [
          'Build Cloud Security Enterprise SaaS product',
          'Ingest Data from Cloud Providers and Perform IAM Risk Analysis',
        ],
        skills: [
          'Python',
          'AWS Cloud',
          'Git',
          'SQL',
          'DynamoDB',
          'Neptune',
          'Docker',
        ],
        icon: '$vuetify.icons.mdiStar',
        color: 'deep-purple darken-3',
      },
      {
        duration: 'April 2021 - August 2022',
        company: 'Axrail Private Limited',
        title: 'Solutions Architect',
        descriptions: [
          'Design Scalable and Secure Applications on AWS',
          'Perform POC on New Technology Stacks or Designs',
          'Develop Cloud Native Applications on AWS',
        ],
        skills: [
          'Python',
          'AWS Cloud',
          'Reactjs',
          'Nodejs',
          'Git',
          'SQL',
          'DynamoDB',
          'OpenSearch',
          'Docker',
        ],
        icon: '$vuetify.icons.mdiStar',
        color: 'amber darken-3',
      },
      {
        duration: 'Aug 2020 - March 2021',
        company: 'Syion Private Limited',
        title: 'Software Engineer',
        descriptions: [
          'Develop Web Applications',
          'Solution implementation with AWS Serverless Architecture',
        ],
        skills: [
          'Python',
          'AWS Cloud',
          'Vuejs',
          'Nodejs',
          'Git',
          'SQL',
          'DynamoDB',
          'Docker',
        ],
        icon: '$vuetify.icons.mdiStar',
        color: 'indigo darken-4',
      },
      {
        duration: 'Aug 2019 - Jul 2020',
        company: 'Keysight Technologies',
        title: 'R&D Software Engineer',
        descriptions: [
          'Develop Desktop Applications using Angular & Modern C++',
          'Develop API services using gRPC',
        ],
        skills: ['C++', 'Python', 'Angular', 'gRPC', 'Agile', 'Git'],
        icon: '$vuetify.icons.mdiStar',
        color: 'deep-purple darken-3',
      },
      {
        duration: 'Jan 2018 - Jul 2019',
        company: 'Keysight Technologies',
        title: 'Test Engineer',
        descriptions: [
          'Develop Test Program using C#, VB6 and VEE Pro',
          'Automate and Modernize Test Stations',
        ],
        skills: ['C#', 'VB6', 'VEE Pro'],
        icon: '$vuetify.icons.mdiStar',
        color: 'amber darken-3',
      },
      {
        duration: 'Dec 2016 - Mar 2017',
        company: 'Keysight Technologies',
        title: 'Intern R&D Engineer',
        descriptions: [
          'Develop and Automate Test Program using VEE pro and VB.Net',
        ],
        skills: ['VEE Pro', 'VB.Net'],
        icon: '$vuetify.icons.mdiStar',
        color: 'indigo darken-4',
      },
    ],
  }),
  methods: {},
}
</script>
