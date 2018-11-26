<template>
	<v-app>
		<my-toolbar :title='title' :links="links"></my-toolbar>

		<v-content>
			<section id="home">
				<v-parallax src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg" height="600">

					<v-layout align-center justify-center column>
						<v-avatar :tile="false" size="128" color="grey lighten-4" >
          					<img src="./assets/photo.jpg" alt="avatar">
        				</v-avatar>
						<br>
						<h1 class="mb-2 display-1 text-xs-center"> {{title}} </h1>
						<div class="subheading mb-3 mr-2 text-xs-center"> {{description}} </div>
					</v-layout>

				</v-parallax>
			</section>

			<section id="projects">
				<my-projects-card></my-projects-card>
			</section>

			<section id="technologies">
				<v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg" height="380">
					<v-layout column align-center justify-center>
							<h1 class="mb-2 display-1 text-xs-center"> Tecnologías </h1>
							<v-layout align-center justify-space-around row fill-height>
								<div class="subheading mb-3 mr-2 text-xs-center"> Vue.js </div>
								<div class="subheading mb-3 mr-2 text-xs-center"> Django </div>
								<div class="subheading mb-3 mr-2 text-xs-center"> Java </div>
								<div class="subheading mb-3 mr-2 text-xs-center"> Mongo </div>
							</v-layout>
					</v-layout>
				</v-parallax>
			</section>

			<section id="contact">
				<my-contact-cards></my-contact-cards>
			</section>

			<section>
				<my-footer :title="title"></my-footer>
			</section>
		</v-content>
	</v-app>
</template>

<script>
	import MyToolbar from './components/MyToolbar'
	import MyContactCards from './components/MyContactCards'
	import MyProjectsCard from './components/MyProjectsCard'
	import MyFooter from './components/MyFooter'

	export default {
		name: "App",
		components: { MyToolbar, MyContactCards, MyProjectsCard, MyFooter },
		data() {
			return {
				title: 'Andrés Aguilar',
				description: 'Ing en TI, 100% pro software libre, usuario GNU/Linux por más de 10 años, programador Sr Python. Apasionado por la tecnología y la lectura.',
				links: [
					{ title: 'Home', icon: 'home', url: '#home' },
					{ title: 'Projects', icon: 'work', url: '#projects' },
					{ title: 'Technologies', icon: 'usb', url: '#technologies' },
					{ title: 'Contact', icon: 'mail', url: '#contact' }
				]
			}
		}
	}
</script>

<style scoped>
	.v-card { box-shadow: none }
	.theme--dark.v-card { background-color: transparent !important }
</style>
