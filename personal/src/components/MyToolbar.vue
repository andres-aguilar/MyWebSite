<template>
    <div>
        <v-toolbar class="white">
            <v-toolbar-title v-text="title"></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat href="#" target="_blank"> <span class="mr-2">Login</span> </v-btn>
        </v-toolbar>
    </div>
</template>

<script>
export default {
    name: 'MyToolbar',
    props: ['title'],
}
</script>
