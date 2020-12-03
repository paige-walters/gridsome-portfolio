<template>
    <section id="projects" class="project-section">
        <v-container>
            <v-row>
                <v-col>
                    <h1>Projects</h1>
                </v-col>
            </v-row>
                <v-row class="justify-space-around mb-8 mt-4">
                        <v-card v-for="project in projects"
                                :key="project.name"
                                    class="mx-auto"
                                    height="350"
                                    max-width="350"
                            >
                            
                                <v-img
                                class="white--text align-end"
                                height="200px"
                                :src="project.image"
                                >
                                <v-card-title>{{project.name}}</v-card-title>
                                </v-img>
                        


                            <v-card-text class="text--primary">
                                {{truncate(project.description)}}
                            </v-card-text>

                            <v-card-actions>
                            <v-btn
                                class="seebutton"
                                text
                                :href="project.github"
                            >
                                See The Code!
                            </v-btn>

                            </v-card-actions>
                        </v-card>
                    </v-hover>
                 </v-row>
        </v-container>
    </section>

</template>

<script>
export default {
    data() {
        return {
            projects: [
                {
                    name: "Personal Project",
                    github: 'https://github.com/paige-walters/personalProject',
                    description: 'Personal project to catalog all stations that contain 93 octane',
                    image: 'https://github.com/paige-walters/precision-polish/blob/main/src/assets/irene1.jpg?raw=true'
                },
                {
                    name: "Precision Polish",
                    github: 'https://github.com/paige-walters/precision-polish',
                    description: 'A site for a car detailing business',
                    image: 'https://github.com/paige-walters/precision-polish/blob/main/src/assets/irene3.jpg?raw=true'
                }
            ]
        }
    },

        methods: {
        truncate(str) {
            if(str.length > 80) {
                return str.slice(0, 79) + '...'
            }
            return str
        }
    }
}


</script>

<style scoped>
.project-section {
    background-color: #A8E6CF;
}
h1 {
    color: #FCF9EC;
}
.seebutton {
    color: #DF8C95;
}
</style>