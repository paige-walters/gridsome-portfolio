<template>
    <section id="education">
        <v-container>
            <v-row>
                <v-col>
                    <h1>Education</h1>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                      <v-timeline>
                        <v-timeline-item
                        v-for="(year, i) in years"
                        :key="i"
                        :color="year.color"
                        small
                        >
                        <template v-slot:opposite>
                            <span
                            :class="`headline font-weight-bold ${year.color}`"
                            v-text="year.year"
                            ></span>
                        </template>
                        <div class="py-4">
                            <h2 :class="`headline font-weight-light mb-4 ${year.color}`">
                            Lorem ipsum
                            </h2>
                            <div>
                            Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
                            </div>
                        </div>
                        </v-timeline-item>
                    </v-timeline>
                </v-col>
            </v-row>
        </v-container>

    </section>
</template>

<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'amber lighten-5',
          year: '2020',
        },
        {
          color: 'blue-grey lighten-5',
          year: '2015',
        },
        {
          color: 'grey lighten-5',
          year: '2010',
        },
        {
          color: 'amber lighten-5',
          year: '2005',
        },
        {
          color: 'blue-grey lighten-5',
          year: '2000',
        },
      ],
    }),
  }
</script>