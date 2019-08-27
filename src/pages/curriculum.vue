<template>
	<v-container fluid grid-list-lg>
		<v-layout row wrap>
			
			<v-flex xs12 sm6 md4 lg3 d-flex v-for="(section, i) in sections" :key="i">
				<v-card raised>
					<v-card-title>
						<div class="headline">{{section.title}}</div>
					</v-card-title>
					<v-container>
						<div v-for="(item, i) in section.items" :key="i">
							<b>{{item.name}}</b><br>
							{{item.desc}}
							<br>
							<b>{{item.val}}</b>
							<br>
							<b>{{item.obs}}</b>
							<div v-if="i != section.items.length - 1">
								<v-divider></v-divider><br>
							</div>
						</div>
					</v-container>
				</v-card>
			</v-flex>
		</v-layout>
	</v-container>
</template>

<script>
export default {
	data: () => ({
		sections: [
			{
				title: 'Computadores',
				items: [
					{
						name: 'Formatação',
						desc: 'Uma formatação vai apagar tudo e reinstalar o sistema do zero. Todos os seus arquivos e configurações serão perdidos, caso não tenha realizado backup nós faremos isto para você. O S.O(Sistema Operacional) será instalado de maneira limpa e tudo deverá ser reconfigurado.',
						val: 'Valor Sugerido : R$ 35,00',
						obs: 'OBS: ATENÇÃO!, O VALOR OU O PRAZO DE ENTREGA PODE VARIAR, POIS PODE-SE LEVAR MAIS TEMPO OU MENOS DEPENDENDO DA CONFIGURAÇÃO DE SEU COMPUTADOR'
					},
					{
						name: 'Limpeza Interna',
						desc: 'Uma limpeza interna em seu computador é tão importante quanto a virtual(formatação, etc...), computadores e notebooks em geral possuem coolers(ventoinhas) para poder tratar o calor interno e não danificar peças e componentes eletrônicos. E também sua saúde é incluída neste tratamento, por conta dos coolers o computador precisa sugar ar de fora para dentro para resfriar o mesmo, logo poeira e outras impurezas no ar são atraídas para perto do usuário.',
						val: 'Valor Sugerido : R$ 30,00'
					},
					{
						name: 'Limpeza Interna + Formatação',
						desc: 'São os dois serviços acima mencionados.',
						val: 'Valor Sugerido : R$ 65,00'
					},
					{
						name: 'Troca de Componentes Internos Danificados',
						desc: 'As vezes temos o azar de algum componente interno vital do computador parar de funcionar por enes motivos, como há muitas peças e componentes o valor e troca dos mesmos pode variar.',
						val: 'Valor Sugerido : VARIÁVEL'
					}

				]
			},
			{
				title: 'Notebooks',
				items: [
					{
						name: 'Formatação',
						desc: 'Uma formatação vai apagar tudo e reinstalar o sistema do zero. Todos os seus arquivos e configurações serão perdidos, caso não tenha realizado backup nós faremos isto para você. O S.O(Sistema Operacional) será instalado de maneira limpa e tudo deverá ser reconfigurado.',
						val: 'Valor Sugerido : R$ 35,00',
						obs: 'OBS: ATENÇÃO!, O VALOR OU O PRAZO DE ENTREGA PODE VARIAR, POIS PODE-SE LEVAR MAIS TEMPO OU MENOS DEPENDENDO DA CONFIGURAÇÃO DE SEU COMPUTADOR'
					},
					{
						name: 'Limpeza Interna',
						desc: 'Uma limpeza interna em seu computador é tão importante quanto a virtual(formatação, etc...), computadores e notebooks em geral possuem coolers(ventoinhas) para poder tratar o calor interno e não danificar peças e componentes eletrônicos. E também sua saúde é incluída neste tratamento, por conta dos coolers o computador precisa sugar ar de fora para dentro para resfriar o mesmo, logo poeira e outras impurezas no ar são atraídas para perto do usuário.',
						val: 'Valor Sugerido : R$ 40,00'
					},
					{
						name: 'Limpeza Interna + Formatação',
						desc: 'São os dois serviços acima mencionados.',
						val: 'Valor Sugerido : R$ 75,00'
					},
					{
						name: 'Troca de Componentes Internos Danificados',
						desc: 'As vezes temos o azar de algum componente interno vital do notebook parar de funcionar por enes motivos, como há muitas peças e componentes o valor e troca dos mesmos pode variar.',
						val: 'Valor Sugerido : VARIÁVEL'
					}
				]
			},
			{
				title: 'Tablets',
				items: [
					{
						name: 'Formatação(Hard Reset)',
						desc: 'Uma formatação(Hard Reset) vai apagar tudo e reinstalar o sistema do zero. Todos os seus arquivos e configurações serão perdidos, caso não tenha realizado backup nós faremos isto para você. O S.O(Sistema Operacional) será instalado de maneira limpa e tudo deverá ser reconfigurado.',
						val: 'Valor Sugerido : R$ 20,00'
					},
					{
						name: 'Limpeza Interna',
						desc: 'A Limpeza interna em tablets e/ou smarthpones não é muito utilizada, mas uma limpeza interna aumenta a vida útil de seu aparelho',
						val: 'Valor Sugerido : R$ 30,00'
					},
					{
						name: 'Limpeza Interna + Formatação',
						desc: 'São os dois serviços acima mencionados.',
						val: 'Valor Sugerido : R$ 50,00'
					},
					{
						name: 'Troca de Componentes Internos Danificados',
						desc: 'As vezes temos o azar de algum componente interno vital do tablet parar de funcionar por enes motivos, como há muitas peças e componentes o valor e troca dos mesmos pode variar.',
						val: 'Valor Sugerido : VARIÁVEL'
					}
				]
			},
			{
				title: 'Smartphones',
				items: [
					{
						name: 'Formatação(Hard Reset)',
						desc: 'Uma formatação(Hard Reset) vai apagar tudo e reinstalar o sistema do zero. Todos os seus arquivos e configurações serão perdidos, caso não tenha realizado backup nós faremos isto para você. O S.O(Sistema Operacional) será instalado de maneira limpa e tudo deverá ser reconfigurado.',
						val: 'Valor Sugerido : R$ 20,00'
					},
					{
						name: 'Limpeza Interna',
						desc: 'A Limpeza interna em tablets e/ou smarthpones não é muito utilizada, mas uma limpeza interna aumenta a vida útil de seu aparelho',
						val: 'Valor Sugerido : R$ 30,00'
					},
					{
						name: 'Limpeza Interna + Formatação',
						desc: 'São os dois serviços acima mencionados.',
						val: 'Valor Sugerido : R$ 50,00'
					},
					{
						name: 'Troca de Componentes Internos Danificados',
						desc: 'As vezes temos o azar de algum componente interno vital do smartphone parar de funcionar por enes motivos, como há muitas peças e componentes o valor e troca dos mesmos pode variar.',
						val: 'Valor Sugerido : VARIÁVEL'
					}
				]
			},
		]
	})
}
</script>
