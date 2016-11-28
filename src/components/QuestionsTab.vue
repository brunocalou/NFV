<template>
	<section class="section--center mdl-layout__tab-panel" id="questions-tab">
		<div class="page-content">
			<h4>Perguntas</h4>

			<ol>
				<li>
					<h5>Por que as funções de rede(NF) em middleboxes possuem um melhor desempenho do que funções de rede virtualizadas(VNF)? E por que uma VNF, mesmo com um pior desempenho em testes, é considerada melhor?</h5>
					<p>Middleboxes são desenvolvidas para uma função específica, utilizando hardware específico para isso. Portanto, o desempenho tende a ser melhor comparado à NFV, que utiliza hardware genérico. O problema é a falta de flexibilidade e adaptabilidade(compatibilidade com camadas superiores). O NFV vem justamente para resolver esses dois grandes problemas das funções de rede atuais.</p>
				</li>
				<li>
					<h5>Quais os benefícios de implantar o NFV e SDN juntos em uma rede?</h5>
					<p>Apesar de serem independentes, o SDN e NFV são complementares. O uso das duas tecnologias, faz com que os recursos de rede sejam melhor aproveitadas, os problemas sejam identificados e resolvidos mais rapidamente, e há uma maior facilidade para inovações, devido às duas tecnologias serem baseadas em software.</p>
				</li>
				<li>
					<h5>Tanto o NFV quanto o SDN são baseados em software. Explique quais as vantagens disso?</h5>
					<p>Possuem maior escalabilidade e baixo custo, o que torna o seu uso atraente tanto para pequenas empresas, que não possuem recursos financeiros abundantes, quanto para grandes empresas, que precisam escalar seus serviços rapidamente.</p>
				</li>
				<li>
					<h5>Quais as principais atribuições da camada de hardware na infraestrutura do NFV e a principal característica desse hardware?</h5>
					<p>A camada de hardware no NFVI inclui recursos de processamento, armazenamento e conectividade através da camada de virtualização. É essencial que esses recursos de hardware sejam de propósito geral, ou COTS (Commercial off-the-shelf).</p>
				</li>
				<li>
					<h5>Qual a diferença entre um hypervisor comum e um hypervisor de NFV?</h5>
					<p>No contexto de NFV, existe conectividade entre as máquinas virtuais. Assim, quando uma VNF se localiza em mais de uma máquina virtual, elas se comunicam diretamente para garantir uma execução eficaz.</p>
				</li>
			</ol>
		</div>
	</section>
</template>