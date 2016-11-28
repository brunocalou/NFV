<template>
<section class="section--center mdl-layout__tab-panel" id="challenges-tab">
	<div class="page-content">
		<h4>Desafios</h4>
		
		<p>Nesse novo paradigma de redes, o trade-off(conflito de escolha) entre desempenho, flexibilidade e segurança é um dos aspectos principais a serem discutidos na virtualização de funções de rede.</p>

		<h5>Desempenho</h5>

		<p>A grande premissa da NFV é utilizar grande volume de servidores de baixo custo. Podendo, assim, desempenhar diversos papéis ao ambiente em que as funções virtuais de rede são implementadas, tornando a alocação de recursos dinâmica. Porém, isso implica que os recursos sejam escaláveis o suficiente para lidar com a grande heterogeneidade dos possíveis serviços oferecidos em uma VNF. Sabendo disso, duas especificações importantes devem ser bem definidas ao instanciar uma VNF: especificações de desempenho e informações coletadas sobre armazenamento, rede e processamento em diferentes níveis de infraestruturas. A especificação de desempenho colabora para que a alocação dinâmica de recurso na infraestrutura da VNF seja feita de forma precisa no momento da instância. Já o monitoramento de forma escalável em diversos níveis de operação e granularidade de VNF’s fornece estados consistentes das funções de rede e seus ambientes. Essas especificações são de fundamental importância para o sucesso e a expansão do conceito NFV.</p>

		<p>Uma aplicação interessante na estrutura de rede atual é a middlebox. É basicamente um software projetado em hardware específico a fim de oferecer alguma função de rede: firewall, IDS, NAT, etc. Nesse caso, o desempenho é bem alto, afinal a tecnologia é projetada especificamente para tal função. A falta de compatibilidade com camadas superiores é o principal problema dessa aplicação. As tecnologias de virtualização terão, no início, desempenho e comportamento inferior comparado a essas middleboxes. Porém, oferecerão a flexibilidade necessária para fornecer elasticidade às funções de rede.</p>

		<p>A figura abaixo propõe uma análise interessante de desempenho entre diferentes chips quando submetidos a casos de alta complexidade. Em todos os chips, conforme a complexidade de uso cresce, o desempenho de todas as soluções decrescem. Porém, os chipsets de propósito único são mais limitados, dificultando e até impossibilitando seu uso em tarefas mais complexas. Já as CPUs genéricas podem se sobressair em desempenho sobre NPUs(e, claro, sobre chipsets específicos) em casos de uso complexos, pelo menos em métricas baseadas em classificação de pacotes(DPI – deep packet inspection).</p>

		<img src="src/components/ChallengesTab/image06.png" alt="">

		<h5>Segurança</h5>

		<p>Tanto a virtualização de alguma função ou serviço sobre alguma infraestrutura quanto a determinação de funções de rede sobre um conjunto de servidores/switches podem favorecer o surgimento de falhas de segurança nos níveis de virtualização do NFV, como também acontecem em sistemas operacionais, cadeias de serviços VNFGs e interface entre funções de rede(NF).</p>


		<p>O NFV dispõe diferentes hierarquias de virtualização, que oferecem múltiplos ambientes de execução possíveis. Cada ambiente virtualizado possui diferentes níveis de desempenho e isolação (incluindo aspectos de segurança). Sabendo disso, provedores de serviços e operadores de rede que utilizam serviços compartilhados, requisitam como principal funcionalidade o isolamento de desempenho entre suas instâncias a fim de que não tenham seus contratos de SLA(acordo de nível de serviço) violados.</p>

		<img src="src/components/ChallengesTab/image13.png" alt="">

		<h5>Resiliência</h5>

		<p>De forma genérica, definimos resiliência como a capacidade de um sistema de se recuperar ou se adaptar às mudanças.</p>

		<p>O mesmo conceito é aplicado em um ambiente de NFV para o caso de falhas em NFs. O modo de recuperação usual adotado é o de recriação das NFs, que pode ocorrer de forma automática ou manual, de acordo com os requisitos dos serviços dependentes dessa função de rede. Portanto é necessário determinar níveis de confiabilidade e disponibilidade para os diferentes serviços, que são constituídos por orquestração de NFVs, de forma a não se tornarem um ponto único de falhas. Uma das técnicas para se evitar um ponto único é a replicação de dados, de forma a garantir a integridade e performance na NFs.</p>

		<p>Diferentes métricas são utilizadas para se medir a resiliência e performance nas NFVs, dentre elas: Taxa máxima de perdas de pacotes não intencional, variação máxima de atraso e latência no fluxo de dados, taxa máxima de falhas de transações válidas e outros. Estes parâmetros definem, por exemplo, a qualidade de serviços como streaming de vídeos, músicas, transações financeiras e aplicações na área de saúde. Resiliência hoje é um dos tópicos mais abordados no que diz respeito a “NFV as a service”.</p>

	</div>
</section>
</template>