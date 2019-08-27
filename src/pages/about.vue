<template>
	<v-container fluid>
		<v-card raised>
			<v-layout row wrap>
				<v-flex xs12 sm4 md3 lg2>
					<v-card-media src="/public/img/avatar2.jpg" height="100%" class="hidden-xs-only"></v-card-media>
					<v-card-media src="/public/img/avatar2.jpg" height="200px" class="hidden-sm-and-up"></v-card-media>
				</v-flex>
				<v-flex xs12 sm8 md9 lg10>
					<v-card-title>
						<div class="headline">{{name}}</div>
					</v-card-title>
					<v-container>
						<p v-html="desc"></p>
						<v-divider></v-divider>
						<div class="headline">{{contact}}</div>
						<v-list ripple>
							<v-list-tile :href="social.facebook" target="_blank">
								<v-list-tile-avatar>
									<v-icon>mdi-facebook</v-icon>
								</v-list-tile-avatar>
								<v-list-tile-title>Facebook</v-list-tile-title>
							</v-list-tile>
							<v-list-tile :href="social.instagram" target="_blank">
								<v-list-tile-avatar>
									<v-icon>mdi-instagram</v-icon>
								</v-list-tile-avatar>
								<v-list-tile-title>Instagram</v-list-tile-title>
							</v-list-tile>
							<v-list-tile :href="`mailto://${social.email}`">
								<v-list-tile-avatar>
									<v-icon>mdi-email</v-icon>
								</v-list-tile-avatar>
								<v-list-tile-title>{{social.email}}</v-list-tile-title>
							</v-list-tile>
							<v-list-tile :href="`tel://${social.phone}`">
								<v-list-tile-avatar>
									<v-icon>mdi-whatsapp</v-icon>
								</v-list-tile-avatar>
								<v-list-tile-title>{{social.phone}}</v-list-tile-title>
							</v-list-tile>
						</v-list>
					</v-container>
				</v-flex>
			</v-layout>
		</v-card>
	</v-container>
</template>

<script>
	export default {
		data: () => ({
			name: 'Shaluna Tech JD',
			contact: 'Contatos',
			desc: `
				Shaluna Tech uma empresa fundada em Brasília-DF, por dois irmãos prestando serviços de assistência técnica em computadores, notebooks e celulares.<br>
				Atualmente a empresa conta com uma loja em João Dourado - BA, localizada na rua "Antônio Nunes, 92 - Centro.<br>
			`,
			social: {
				facebook: 'https://www.facebook.com/shalunatechjd',
				email: 'shalunatechjd@gmail.com',
				phone: '(74)9 9975-6669 / (74)9 9985-3131',
				instagram: 'https://www.instagram.com/shalunatechjd'
			}
		})
	}

	function idade(d, m, y){
		let D = new Date()
		let cY = D.getFullYear()
		let cM = D.getMonth() + 1
		let cD = D.getDate()
		let age = cY - y
		if(cM < m || cM == m && cD < d){
			age--
		}
		return age
	}
</script>
