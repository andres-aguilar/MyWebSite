<template>
    <div>
        <v-container grid-list-xl>
            <v-layout row wrap justify-center class="my-5">

                <v-flex xs12 sm4>
                    <v-card class="elevation-0 transparent">
                        <v-card-title primary-title class="layout justify-center"> 
                            <div class="headline"> {{ company.title }} </div> 
                        </v-card-title>
                        
                        <v-card-text> {{ company.text }} </v-card-text>
                      </v-card>
                </v-flex>

                <v-flex xs12 sm4 offset-sm1>
					<v-card class="elevation-0 transparent">
						<v-card-title primary-title class="layout justify-center">
							<div class="headline">Contact us</div>
                        </v-card-title>

                        <v-card-text>
							Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                        </v-card-text>

                        <v-list class="transparent">

							<v-list-tile v-for="el in contact" :key="el.id">
								<v-list-tile-action>
									<v-icon class="blue--text text--lighten-2"> {{ el.icon }} </v-icon>
								</v-list-tile-action>
								<v-list-tile-content>
									<v-list-tile-title> {{ el.text }} </v-list-tile-title>
								</v-list-tile-content>
							</v-list-tile>

                        </v-list>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </div>
</template>

<script>
export default {
	name: 'MyContactCards',
	data() {
		return {
			company: { title: 'Company Info', text: 'Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.' },
			contact: [
				{ id: 1, icon: 'phone', text: 'XXX-XXX-XXXX' },
				{ id: 2, icon: 'place', text: 'Puebla, México' },
				{ id: 3, icon: 'email', text: 'andres-aguilar.com' },
			]
		}
	}
}
</script>

