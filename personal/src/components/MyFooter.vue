<template>
    <v-footer dark height="auto" >
    <v-card flat tile class="indigo lighten-1 white--text text-xs-center" >
      <v-card-text>
        <v-btn v-for="(sm, i) in social_media" :key="i" class="mx-3 white--text" icon >
            <a class="icono" :href="sm.url" target="_blank">
                <v-icon size="24px">{{ sm.icon }}</v-icon>
            </a>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        &copy;2018 — <strong> {{ title }} </strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
    export default {
        props: ['title'],
        data: () => ({
            social_media: [
                //{icon: 'fab fa-facebook', url: '#'},
                {icon: 'fab fa-twitter', url: 'https://twitter.com/nano_yosh'},
                {icon: 'fab fa-github', url: 'https://github.com/andres-aguilar'},
                {icon: 'fab fa-linkedin', url: 'https://www.linkedin.com/in/aguilar-salgado-andres/'},
                //{icon: 'fab fa-instagram', url: ''},
            ]
        })
    }
</script>

<style scoped>
    .icono {
        text-decoration: none;
        color: white
    }
</style>
