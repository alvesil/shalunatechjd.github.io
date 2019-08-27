<template>
	<v-container fluid>
		<v-list>
			<v-list-tile v-for="(certificate, i) in certificates" :key="i" ripple :href="certificate.file" target="_blank">
				<v-list-tile-avatar>
					<v-icon>mdi-download</v-icon>
				</v-list-tile-avatar>
				<v-list-tile-title>{{certificate.name}}</v-list-tile-title>
			</v-list-tile>
		</v-list>
	</v-container>
</template>

<script>
	export default {
		data: () => ({
			certificates: [
				{
					name: 'Certificado de Conclusão do Ensino Médio (Centro de Ensino Médio 12 de Ceilândia)',
					file: '/public/doc/certificates/certificado_de_conclusão_do_ensino_médio_CEM12.jpg'
				},
				{
					name: 'Estágio Supervisionado em Telecomunicações (Escola Técnica de Brasília)',
					file: '/public/doc/certificates/estágio_supervisionado_ETB.jpg'
				},
				{
					name: 'Assistente Técnico de Planejamento e Projetos em Telecomunicações (Escola Técnica de Brasília)',
					file: '/public/doc/certificates/assistente_técnico_de_planejamento_e_projetos_em_telecomunicações_ETB.jpg'
				},
				{
					name: 'Assistente Técnico de Manutenção em Telecomunicações (Escola Técnica de Brasília)',
					file: '/public/doc/certificates/assistente_técnico_de_manutenção_em_telecomunicações_ETB.jpg'
				},
				{
					name: 'Operador em Telecomunicações/ Informação e Comunicação (Escola Técnica de Brasília)',
					file: '/public/doc/certificates/operador_em_telecomunicações_informação_e_comunicaçõe_ETB.jpg'
				},
				{
					name: 'Técnico em Telecomunicações/ Informação e Comunicação (Escola Técnica de Brasília)',
					file: '/public/doc/certificates/técnico_em_telecomunicações_informação_e_comunicaçõe_ETB.jpg'
				},
				{
					name: 'Programador de Aplicativo Android - Básico - (#BORA VENCER)',
					file: '/public/doc/certificates/android_BORAVENCER.jpg'
				},
				{
					name: 'Conecta IF - 2017 (Instituto Federal de Ciência e Tecnologia de  Brasília)',
					file: '/public/doc/certificates/conecta_if_2017_IFB.pdf'
				},
				{
					name: 'Conecta IF - 2018 (Instituto Federal de Ciência e Tecnologia de  Brasília)',
					file: '/public/doc/certificates/conecta_if_2018_IFB.pdf'
				},
				{
					name: 'Qualific Express - Ensino de Física e Computação Usando Impressora 3D e Arduíno - (Instituto Federal de Ciência e Tecnologia de  Brasília)',
					file: '/public/doc/certificates/Ensino_de_Física_e_Computação_usando_impressora_3D_e_arduíno_QUALIFICEXPRESS.pdf'
				}
			]
		})
	}
</script>
