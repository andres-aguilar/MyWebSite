<template>
    <nav>
        <v-toolbar fixed class="hidden-sm-and-down">
            <v-toolbar-title v-text="title"></v-toolbar-title>
            <v-spacer></v-spacer>

            <v-btn v-for="(link, i) in links" :key="i" flat :href="link.url">
                <v-icon> {{ link.icon }} </v-icon>
                <span class="mr-2"> {{ link.title }} </span> 
            </v-btn>

        </v-toolbar>

        <div class="hidden-md-and-up">
            <v-toolbar fixed color="primary" :dark="true">
                <v-toolbar-title> {{ title }} </v-toolbar-title>
                <v-spacer></v-spacer>
                <v-toolbar-side-icon @click.stop="drawer = !drawer"> </v-toolbar-side-icon>
            </v-toolbar>
        </div>

        <v-navigation-drawer v-model="drawer" absolute temporary>
            <v-list class="pa-1">
                <v-list-tile avatar>
                <v-list-tile-avatar>
                    <img src="../assets/photo.jpg">
                </v-list-tile-avatar>

                <v-list-tile-content>
                    <v-list-tile-title> {{ title }} </v-list-tile-title>
                </v-list-tile-content>
                </v-list-tile>
            </v-list>

            <v-list class="pt-0" dense>
                <v-divider></v-divider>

                <v-list-tile v-for="item in links" :key="item.title">

                    <v-list-tile-action>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-tile-action>

                    <v-list-tile-content>
                        <v-list-tile-title> <a class="menu-link" :href="item.url"> {{ item.title }} </a> </v-list-tile-title>
                    </v-list-tile-content>

                </v-list-tile>
            </v-list>
        </v-navigation-drawer>

    </nav>
</template>

<script>
export default {
    name: 'MyToolbar',
    props: ['title', 'links'],
    data () {
      return { drawer: null, }
    }
}
</script>

<style scoped>
    .menu-link {
        text-decoration: none;
        font-size: 1.2em;
        color: inherit
    }
</style>
