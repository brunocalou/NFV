<template>
<section class="section--center mdl-layout__tab-panel" id="virtualization-tab">
  <div class="page-content">
	
	<h4>Virtualização</h4>

	<p>Virtualização pode ser definida como a criação de uma versão virtual de algo. Geralmente, são virtualizados sistemas operacionais, recursos de rede, plataformas de hardware e dispositivos de armazenamento. Podemos ver na imagem abaixo dois tipos de virtualização (tipo bare-metal e tipo hosted), onde em um mesmo hardware vários sistemas operacionais são executados simultaneamente e de forma independente. Note que há uma camada compartilhada de virtualização (<a href="#hypervisor">Hypervisor</a>) que é utilizada por todos os sistemas operacionais virtualizados.</p>

	<img src="src/components/VirtualizationTab/image05.png" alt="">

	<p>Sem a virtualização, é necessário uma máquina para rodar cada sistema e, como o sistema não usa todos os recursos disponíveis, uma grande parte deles se torna ocioso, o que desperdiça energia e recursos. A virtualização traz consigo a possibilidade de utilizar recursos de hardware de maneira otimizada, de forma que  vários sistemas podem ser executados no mesmo hardware. Consequentemente, os recursos podem ser alocados dinamicamente para cada sistema, de forma a evitar ociosidade. Além disso, a virtualização permite uma rápida escalabilidade devido à sua natureza “elástica”. Por exemplo, digamos que existam vários sistemas operacionais convidados (guest) em uma mesma máquina, todos virtualizados e controlados pelo hypervisor; Se um dos sistemas exigir mais recursos, como processamento ou memória por exemplo, é possível realocar os recursos de forma que esse sistema use os recursos necessários para sua demanda e os outros não sejam prejudicados.</p>

	<h4>Funções de Rede Virtualizadas - VNF</h4>

	<p>No contexto de virtualização de recursos de rede, ao invés de virtualizar sistemas operacionais, virtualizam-se funções de rede, como firewall, balanceador de carga, CDN, IDS, etc. O que antes era executado por hardwares especializados passa a ser executado em computadores de uso genérico, de forma que os problemas relacionados em manter recursos de redes físicas desaparecem. Com as funções virtualizadas, não é mais necessário comprar equipamentos caros e integrá-los, basta utilizar computadores de uso comum para ter acesso às funções de rede necessárias.</p>

	<img src="src/components/VirtualizationTab/image04.png" alt="">

	<h4>NFV como um Serviço - NFVaaS</h4>

	<p>Ao utilizar NFV como serviço, vários clusters na nuvem são utilizados para prover serviços de virtualização facilmente escaláveis e com baixo custo. Desta forma, se os recursos de uma máquina estiverem completamente utilizados, basta alocar mais uma máquina para poder ter mais sistemas em funcionamento. Além disso, máquinas podem ser usadas para duplicar o estado de um sistema e acabar com o ponto único de falha, de forma que se uma máquina falhar, uma outra máquina pode recuperar o sistema no mesmo instante de forma transparente.</p>

	<p>Como as máquinas e os sistemas de gerenciamento são controlados pelo provedor do serviço, alocar recursos passa ser tão simples quanto apertar um botão. Sem o NFV, escalar um sistema envolve comprar o equipamento necessário, instalá-lo e integrá-lo ao sistema, além de dar manutenção e manter uma equipe capaz de lidar com as quaisquer problemas que os equipamentos possam apresentar. Logo, ao utilizar NFV como serviço, torna-se claro que a escalabilidade é um dos pontos fortes do NFV e o motivo dele ser tão atrativo.</p>

	<h4>Infraestrutura NFV - NFVI</h4>

	<p>Definimos “Network Function Virtualization Infrastructure” (NFVI) como o conjunto de componentes de Software e Hardware na qual podemos implementar, executar e gerenciar uma função de rede (NF). A NFVI pode ser composta de múltiplos pontos de presença (NFVI-PoP), que são localidades onde uma NF é implementada ou como função física (PNF) ou virtual de rede (VNF). A rede que provê conectividade entre esses pontos também é de responsabilidade do design de projeto da NFVI.</p>

	<p>A camada de hardware no NFVI inclui recursos de processamento, armazenamento e conectividade através da camada de virtualização. É essencial que esses recursos de hardware sejam de propósito geral, ou COTS (Commercial off-the-shelf). Interconectando esses recursos, há dois tipos de redes: NFVI-PoP e as redes de transporte que os interconectam.</p>

	<p>Outra importante camada em NFVU é a de virtualização, que abstrai os recursos de hardware e desacopla o software, garantindo independência do hardware a ser utilizado. O desacoplamento, em geral, é possível com hypervisors que são uma das soluções mais atuais para tal camada. O VMWare, por exemplo, que permite a execução de diversas máquinas virtuais em máquinas de propósitos gerais. Para conectividade, a virtualização de recursos de redes inclui técnicas como: VxLANs e OpenFlow.</p>

	<h4 id="hypervisor">Hypervisor</h4>

	<p>Uma das principais características do NFV é o desacoplamento das funções de rede dos hardwares especializados, possibilitando o uso de hardwares de propósito geral. Para obter essa vantagem, é necessário criar uma camada de virtualização na infraestrutura de NFV através do particionamento lógico dos recursos (slicing) entre as funções de rede virtuais. Este desacoplamento dos recursos de computação e armazenamento do software é realizado por meio de hypervisors.</p>

	<p>Sucintamente, um hypervisor é um programa que provém uma camada de abstração para o hardware de rede, permitindo execução de diversas máquinas virtuais em hardware de propósito geral no contexto de NFV.</p>

	<img src="src/components/VirtualizationTab/image00.png" alt="">

	<p>Mesmo não existindo um padrão para a abstração em NFV, o uso de hypervisors é bem comum. Por exemplo, uma função de rede virtual pode ser executada em uma ou mais máquinas virtuais. Para uma execução eficiente, deve haver conectividade entre as máquinas virtuais. Através dos hypervisors de NFV, é possível criar uma permissividade de acesso direto às funções de rede ou uma comunicação direta entre máquinas virtuais. Várias técnicas são implementadas neste âmbito, tais como VxLANs (Virtual Extensible Local Area Network), NVGRE (Network Virtualization using Generic Routing Encapsulation) e OpenFlow.</p>

	<h4>Orquestrador</h4>

	<p>Uma vantagem de usar NFV é a entrega de serviços de hardware industrial por meio de software. Este modelo entrega serviços mais rápidos e com mais flexibilidade. Porém, isso gera uma demanda considerável por recursos virtuais, necessitando de um gerenciamento de alto nível para manter a funcionalidade da rede. Este gerenciamento é chamado de orquestração.</p>

	<p>Para tanto, a orquestração se constrói com base no modelo dos hypervisor e outros softwares próprios para gerenciamento (vSphere, OpenStack, CloudStack). Assim, têm-se o Orquestrador de NFV, responsável por orquestrar e gerenciar de forma ampla os recursos de NFV (infraestrutura e software). Ele possui o controle e a visibilidade da topologia de serviços e de todas as funções de rede virtualizadas sendo executadas dentro da infraestrutura de NFV.</p>

	<img src="src/components/VirtualizationTab/image06.png" alt="">

	<p>Esse sistema cuida para que as máquinas virtuais e as funções de rede estejam otimizadas em suas funcionalidades e de acordo com o ambiente em que se encontram. Um desafio apresentado por isso é a migração dessas funções, requerendo a manutenção de seu estado durante sua realocação, replicação ou qualquer tipo de gerenciamento de escalabilidade. Agregadas a estes serviços estão as tarefas de detecção, diagnóstico e recuperação de falhas. Cabe ao orquestrador verificar a integridade operacional da infraestrutura de NFV em todos os níveis de aplicação.</p>

  </div>
</section>
</template>