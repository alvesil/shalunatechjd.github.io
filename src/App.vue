<template>
	<v-app>
		<v-jumbotron height="auto" src="/public/img/cover.jpg" dark>
			<v-container fill-height>
				<v-layout column align-center>
					<v-avatar size="200px" class="mt-5 mb-5">
						
					</v-avatar>
				</v-layout>
			</v-container>
		</v-jumbotron>
		<v-toolbar color="black" dark class="elevation-0" ref="toolbar" :fixed="offsetTop >= 328" v-scroll="onScroll">
			<v-toolbar-side-icon class="hidden-sm-and-up" @click="drawer = !drawer"></v-toolbar-side-icon>
			<v-toolbar-title>{{name}}</v-toolbar-title>
			<v-spacer></v-spacer>
			<v-toolbar-items class="hidden-xs-only">
				<v-btn flat to="/about">Sobre</v-btn>
				<v-btn flat to="/curriculum">Serviços</v-btn>
				<v-btn flat to="/projects">Produtos</v-btn>
				<!--<v-btn flat to="/certificates">Certificados</v-btn>-->
			</v-toolbar-items>
		</v-toolbar>
		<v-content>
			<transition name="fade">
				<router-view></router-view>
			</transition>
		</v-content>
		<v-bottom-sheet v-model="drawer">
			<v-list>
				<v-list-tile ripple to="/about" @click="drawer = false">
					<v-list-tile-title>Sobre</v-list-tile-title>
				</v-list-tile>
				<v-list-tile ripple to="/curriculum" @click="drawer = false">
					<v-list-tile-title>Serviços</v-list-tile-title>
				</v-list-tile>
				<v-list-tile ripple to="/projects" @click="drawer = false">
					<v-list-tile-title>Produtos</v-list-tile-title>
				</v-list-tile>
				<v-list-tile ripple to="/certificates" @click="drawer = false">
					<v-list-tile-title>Certificados</v-list-tile-title>
				</v-list-tile>
			</v-list>
		</v-bottom-sheet>
		<v-footer color="lime accent-4">
			<v-spacer></v-spacer>
			&copy; {{name}} {{year}}
			<v-spacer></v-spacer>
		</v-footer>
	</v-app>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active {
	transition: opacity .3s;
}
.fade-enter, .fade-leave-to {
	opacity: 0;
}
</style>

<script>
export default {
	data: () => ({
		offsetTop: 0,
		drawer: false,
		name: 'Shaluna Tech JD'
	}),
	methods: {
		onScroll(e){
			this.offsetTop = window.pageYOffset || document.documentElement.scrollTop
		}
	},
	computed: {
		width(){
			return innerWidth
		},
		year(){
			return new Date().getFullYear()
		}
	}
}
</script>
