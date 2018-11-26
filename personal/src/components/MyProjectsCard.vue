<template>
    <div>
        <v-layout column wrap class="my-5" align-center >
            <v-flex xs12 sm4 class="my-3">
                <div class="text-xs-center">
                    <h2 class="headline"> {{ title }} </h2>
                    <span class="subheading"> {{ subtitle }} </span>
                </div>
            </v-flex>

            <v-flex xs12>
                <v-container grid-list-xl>
                    <v-layout row wrap align-center>

                        <v-flex xs12 md4 v-for="project in projects" :key="project.id">
                            <v-card class="elevation-0 transparent">

                                <v-card-text class="text-xs-center">
                                    <v-icon x-large class="blue--text text--lighten-2"> {{ project.icon }} </v-icon>
                                </v-card-text>

                                <v-card-title primary-title class="layout justify-center">
                                    <div class="headline text-xs-center"> {{ project.title }} </div>
                                </v-card-title>
                                
                                <v-card-text> {{ project.text }} </v-card-text>
                            </v-card>
                        </v-flex>

                    </v-layout>
                </v-container>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
export default {
    name: 'MyProjectsCard',
    data() {
        return {
            title: 'Proyectos',
            subtitle: 'Algunos de los proyectos en los que he participado',
            projects: [
                { id: 1, icon: 'blur_linear', title: 'ImmunediveRsity', text: 'Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.' },
                { id: 2, icon: 'power_input', title: 'Helitrons', text: 'Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.' },
                { id: 3, icon: 'cloud_queue', title: 'WebScrappers', text: 'Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.' },
                { id: 4, icon: 'gps_not_fixed', title: 'ShootSoft', text: 'Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.' },
            ]
        }
    }
}
</script>

<style>

</style>
