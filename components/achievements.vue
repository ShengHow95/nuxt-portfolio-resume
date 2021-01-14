<template>
  <v-container>
    <v-card>
      <v-card-title class="justify-center font-weight-bold">
        <v-icon large color="white">$vuetify.icons.mdiMedal</v-icon>
        &nbsp; ACHIEVEMENTS
      </v-card-title>
      <v-card-text>
        <v-expansion-panels>
          <v-expansion-panel v-for="(timeline, i) in timelines" :key="i">
            <v-expansion-panel-header class="text-subtitle-1">
              Year {{ timeline.year }}
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-list-item
                v-for="(achievement, j) in timeline.achievements"
                :key="j"
                class="text-subtitle-1"
              >
                <v-list-item-content>
                  {{ achievement.name }}
                </v-list-item-content>
                <v-list-item-action>
                  <v-btn
                    outlined
                    color="grey"
                    :href="achievement.link"
                    target="_blank"
                    :disabled="achievement.disabled"
                    rel="noreferrer"
                  >
                    <v-icon>$vuetify.icons.mdiLink</v-icon>
                  </v-btn>
                </v-list-item-action>
              </v-list-item>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    timelines: [
      {
        year: 2020,
        achievements: [
          {
            name: 'Fake News Detection Using Deep Learning',
            publisher:
              '2020 IEEE 10th Symposium on Computer Applications & Industrial Electronics (ISCAIE)',
            link: 'https://ieeexplore.ieee.org/document/9108841',
            disabled: false,
          },
        ],
      },
      {
        year: 2018,
        achievements: [
          {
            name: 'Sarawak Energy’s Best Final Year Project Award',
            publisher: 'Sarawak Energy',
            link:
              'https://www.sarawakenergy.com/media-info/media-releases/2018/sarawak-energy-rewards-curtin-top-students',
            disabled: false,
          },
          {
            name: 'Sarawak Energy’s Best Graduate Award',
            publisher: 'Sarawak Energy',
            link:
              'https://www.sarawakenergy.com/media-info/media-releases/2018/sarawak-energy-rewards-curtin-top-students',
            disabled: false,
          },
          {
            name: 'IEEE Malaysia Student Volunteer Award',
            publisher: 'IEEE Malaysia Section',
            link: '',
            disabled: true,
          },
          {
            name: 'IEEE R10 Student Activities Committee Volunteer Award',
            publisher: 'IEEE Region 10',
            link: '',
            disabled: true,
          },
        ],
      },
      {
        year: 2017,
        achievements: [
          {
            name: 'Innovate Malaysia 2017 - Keysight Track [Champion]',
            publisher: 'Dream Catcher',
            link:
              'https://international.curtin.edu.my/news/curtin-malaysia-team-champion-of-keysight-track-in-innovate-malaysia-design-competition/',
            disabled: false,
          },
          {
            name: 'IEEE Curtin Malaysia Student Branch President',
            disabled: true,
          },
          {
            name: 'IEEE R10 Sub-Zonal Student Representative',
            disabled: true,
          },
        ],
      },
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
