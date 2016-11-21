<template>
<section class="section--center mdl-layout__tab-panel" id="virtualization-tab">
  <div class="page-content">
	<h4>Virtualização</h4>
	<p>Há basicamente três tipos de soluções em virtualização que atender a infraestrutura de TI, que são:
		<ul>
			<li>Virtualização de servidores</li>
			<li>Virtualização de aplicativos</li>
			<li>Virtualização de desktops</li>
		</ul>
	</p>
	
	<p>Antes de detalhar cada solução, vale a pena definir exatamente o que é o conceito de virtualização:
	</p>
	
	<h5>O que é virtualização?</h5>
	
	<p>A resposta acadêmica mais adequada para esta pergunta é:</p>
	
	<p><strong>Abstração de uma camada física para múltiplas camadas lógicas.</strong></p>
	
	<p>Em outras palavras, virtualização é a solução / conceito de ter uma unidade de algo e logicamente (durante seu funcionamento/produção) ter múltiplas unidades.
	</p>
	
	<p>Se for realizada uma boa análise das soluções em TI no decorrer dos anos, teremos a certeza de que já utilizamos este conceito há muito tempo. Posso exemplificar com 2 soluções utilizadas em praticamente todos ambientes de TI que conheço, uma delas inclusive é muito utilizado em computadores domésticos, que são VLANs e Particionamento de Disco, conforme podemos ver nas imagens abaixo:		
	</p>
	
	<img src="src/components/VirtualizationTab/image12.png" alt="">
	<img src="src/components/VirtualizationTab/image10.png" alt="">

	<p>No caso de VLANs, seu funcionamento basicamente resume-se em ter uma unidade de switch e um número determinado de portas (12, 24, 48) e logicamente criar N redes distintas, algo muito utilizado em infraestruturas de TI segmentadas, com redes distintas para produção, gerência e homologação por exemplo.
	</p>

	<p>Já no caso do particionamento, ação conhecida e bastante utilizada também por público doméstico durante instalação de um sistema operacional, onde o HD de 500GB por exemplo é divido em duas partições lógicas (C e D), sendo uma para arquivos de sistemas e outra para documentos diversos, trazendo assim um nível de segurança e acessibilidade.
	</p>

	<p>Sabemos agora que o conceito de virtualização e usado desde os tempos modernos da TI, porém sem a nomenclatura utilizada hoje. Vamos agora entender as principais diferenças e aplicações dos três tipos de virtualização mais utilizados em infraestrutura de TI.
	</p>

	<h5>Virtualização de Servidores</h5>

	<p>Conhecidos como hypervisor, são sem dúvida o mais usado entre os três. Tem como líder do mercado a solução ESX (Vsphere) da Vmware, porém grandes concorrentes de ponta como XenServer (Citrix System) e Hiper-V (Microsoft).
	</p>

	<p>O hypervisor é um sistema operacional funcional, ou seja, ele substitui integralmente aquele padrão de instalação dos sistemas operacionais convencionais, como Windows Server, Linux, Novell e etc, como podemos ver na imagem abaixo:
	</p>
	
	<img src="src/components/VirtualizationTab/image11.png" alt="">


	<p>Conforme podemos ver no desenho da solução da VMware, há uma camada de virtualização substituindo o sistema operacional tradicional, que proporciona, através de sua tecnologia, criar múltiplas máquinas virtuais, totalmente independente de seus recursos.
	</p>

	<p>Existem N vantagens e discursos comerciais para aderência desta solução, desde ganhos em economia de energia, espaço físico, tempo X foco, green it, mas para mim, o mais importante de todos é o ganho em performance.
	</p>

	<p>Pegamos por exemplo um Windows Server 2008 R2, que será instalado para prover solução de sistema diretório (Active Directory), DNS e DHCP. Obviamente, seus recursos serão focados para prover estas funções, não fazendo uso de todos os recursos do hardware, sem falar também que muitas vezes, por conta de serviços conflitantes, é necessária a criação de vários servidores em hardwares distintos. É provado, através de testes e pesquisas, que quando utilizado um sistema operacional tradicional, a utilização dos recursos físicos do hardware chega no máximo à 20%, tornando assim seu investimento caro e sem uso total.
	</p>

	<p>Quando utilizado uma solução de hypervisor, seu aproveitamento de recursos do hardware sai dos 20% para 80 ou 90%. Isso acontece pois o hypervisor tem por essência esta função, de prover todos os recursos e gerenciar seu funcionamento, provendo também outras soluções, como quebra da incompatibilidade de recursos  no mesmo servidor, pois é possível criar N servidores virtuais em um único hardware.
	</p>

	<p>Essas são algumas das vantagens na solução de hypervisor, onde também cada fabricante tem características particulares para oferecer.
	</p>

	<h5>Virtualização de Aplicativos</h5>

	<p>Prática pioneira da Citrix System, com soluções para esta demanda desde 1996 com o Citrix (Winframe) Metaframe. Com o passar dos anos, foram apresentadas grandes melhorias, como acesso WEB, acesso seguro e legado, de tal forma que grandes concorrentes foram ganhando Mercado.
	</p>

	<p>Em meados dos anos 90 a empresa americana Citrix System desenvolveu e apresentou ao mercado seu produto inovador, um produto capaz de “virtualizar” aplicações, seja ela qual for, com a apenas a premissa de a mesma ser uma aplicação multi usuário, veja desenho:
	</p>

	<img src="src/components/VirtualizationTab/image02.png" alt="">

	<p>Basicamente, virtualização de aplicações é a possibilidade de acessar, utilizar e ser produtivo em aplicações de forma remota, sem a necessidade da instalação da mesma na máquina na qual pode estar usando. Primeiramente, este acesso era feito apenas em LAN ou através de VPN, sendo obrigado a configuração de um cliente, como se fosse um daqueles discadores antigos de internet via ADSL Modem, mas com o surgimento do mundo Web, hoje é possível o acesso via internet, de forma simples, fácil e segura, com possibilidades até de acessos mobile através de smartphones e tablets.
	</p>

	<p>Seu funcionamento é bastante simples, hoje em um ambiente tradicional corporativo, a arquitetura técnica dos aplicativos é descentralizada, ou seja, cada máquina tem seu “arsenal” de aplicativos instalados localmente, como podemos ver na imagem abaixo:
	</p>

	<img src="src/components/VirtualizationTab/image01.png" alt="">

	<p>Já no ambiente virtualizado esta arquitetura é diferente. São criados servidores onde serão centralizados todos os aplicativos do ambiente. A partir de sua tecnologia estes aplicativos são entregues, seja em LAN ou WAN, de forma segura e performática, veja na imagem abaixo:
	</p>
	
	<img src="src/components/VirtualizationTab/image00.png" alt="">

	<p>Todo o processamento é realizado nos servidores onde foram instalados os aplicativos,  desta forma o acesso é rápido e bastante seguro, tornando bastante possível o acesso de devices distintos, como por exemplo, o acesso de aplicativos de legado Microsoft, como Office, Dynamics e etc, em dispositivos com Android, IOS, Linux e ThinClient.
	</p>

	<p>Além do Citrix XenApp (antigo metaframe) existem outros fabricantes com esta solução, como Tarantela, Go-Global e Windows Server, com features de publicação de aplicativos, porém o Citrix neste quesito é líder e contém o produto mais estável e performático.
	</p>

	<h5>Virtualização de Desktop</h5>

	<p>O caçula do mundo de virtualização, porém o grande inovador e de ótima aceitação. Produtos como Citrix XenDesktop e Vmware View além de melhorar o dia-a-dia do TI, traz mobilidade, flexibilidade e produtividade para o negócio.
	</p>

	<p>Com aceitação das soluções de virtualização de servidores e aplicativos, surgiu a necessidade de ampliar este conceito, e juntamente com a demanda do mercado de TI e a velocidade das áreas de negócios, surgiu a virtualização de desktops.
	</p>

	<p>Seu conceito é baseado no funcionamento da virtualização de aplicativos, porém sua centralização é realizada em um hypervisor e seu dado centralizado são desktops, ou seja, em um ambiente com desktops virtuais, o Windows Professional (por exemplo) não fica mais instalado localmente, mas sim, instalados na solução de hypervisor e distribuído, através de diretrizes, por um broker centralizador, veja imagem abaixo:
	</p>

	<img src="src/components/VirtualizationTab/image14.png" alt="">

	<p>A entrega dos desktops para  o usuário pode ser via MAC Address de sua estação, sendo ela um desktop convencional, um notebook, ThinClient ou até mesmo um desktop sem uso de HD (o boot pode ser realizado via PXE) ou via web, que possibilidade acesso de desktop virtual via internet, sem a necessidade de VPN ou clientes específicos de acesso externo.
	</p>

	<p>Hoje, empresas como engenharias, construtoras, call center e empresas que necessitam de acesso importantes de profissionais estratégicos utilizam fielmente soluções de virtualização de desktop. Podemos ter o exemplo de uma construtora que contém um time de engenheiros em obras fora de sua sede, com apenas um container, um link (banda larga ou 3G) já trabalhando como se estivessem localmente no escritório, e podendo até usar ThinClient como seu desktop, economizando energia e alguns caso geradores.
	</p>

	<p>Foi esta solução que tornou possível e bem acessível o conceito BYOD – Bring Your Own Devive, onde a empresa não dita que tipo de device o usuário terá, ele pode por exemplo trazer seu notebook ou tablet pessoal, e através do Citrix XenDesktop, por exemplo, o desktop que ele trabalhará será entregue de forma virtual, ou por exemplo, é possível trabalho 100% produtivo via home office.
	</p>

	<p>Hoje o líder neste segmento, seguindo o exemplo da virtualização de aplicativos, é a Citrix System, por conta de seu pioneirismo e assembly de seu protocolo (ICA-TCP), mas a Vmware está logo atrás com o Vmware View (PC-over-IP).
	</p>

	<p>Bom, basicamente são as três principais  soluções mais utilizadas no mercado, e mesmo com seu crescimento há muita dificuldade em seu entendimento, onde é gerado desconfiança  e como já comentado e outros artigos, é desenhado ou desejado por empresas uma solução de virtualização onde outra seria a aderente à sua necessidade.
	</p>

	<h5>Funções de Rede Virtualizadas (VNF)</h5>

	<p>VNF é a virtualização de funções de redes. Exemplos de funções de rede incluem as desempenhadas por roteadores, firewalls, gateways residenciais, elementos da arquitetura 3GPP como o MME (Mobility Management Entity), PGW (Packet Data Network Gateway), servidores de autenticação, servidores DHCP, entre outros. Uma função de rede pode ser decomposta em diferentes componentes externos, os quais podem ser implementados em diferentes máquinas virtuais. No entanto, o comportamento funcional de uma função de rede deve ser independente, se tal função é virtualizada em múltiplas VMs, em uma única VM ou não é virtualizada.
	</p>

	<img src="src/components/VirtualizationTab/image05.png" alt="">

	<h5>Virtual Network Functions as a Service (VNFaaS)</h5>

	<p>Atualmente muitas empresas estão implantando mais serviços nas bordas de suas redes. Apesar desse comportamento, a utilização de equipamentos dedicados e seu alto custo, inflexibilidade tecnológica, demora na instalação e  dificuldade de manutenção, dificultam esse processo. Como as necessidades tecnológicas continuam evoluindo, mais serviços e aplicações migram para os centros de dados ou nuvens públicas, provocando constantes mudanças na estrutura das redes corporativas. Todas essas mudanças requerem constantes investimentos, forçando as empresas a procurarem alternativas de terceirização do fornecimento dos serviços de tecnologia. Nesse cenário, a virtualização do CPE nos provedores de serviço tornou-se uma alternativa, visto que os clientes não precisam mais arcar com os custos do ciclo de vida da tecnologia, enquanto os provedores aproveitam eficientemente os recursos existentes em seus centros de dados, virtualizando recursos com o NFV.
	</p>

	<img src="src/components/VirtualizationTab/image04.png" alt="">

	<p>No VNFaaS, o serviço NFV fornecido pelo provedor é semelhante ao SaaS da computação em nuvem. A VNF é a aplicação do provedor, a empresa é o cliente do serviço e ela não tem acesso direto ou administrativo ao NFVI ou NFV, sendo apenas a consumidora do VNFaaS. Nesse ambiente, as operadoras podem virtualizar o próprio roteador de borda (PE), apesar de que há maiores vantagens em virtualizar o CPE por motivos de haver um número muito maior de CPEs e sua atuação ser apenas local.
	</p>

	<p>O vE-CPE pode substituir todo um conjunto de equipamentos existentes no lado do cliente por soluções de NFV localizados nos provedores de nuvem ou nos centros de dados dos provedores de serviços. o vE-CPE é capaz de prover serviços de roteamento  com QoS, firewall nas 7 camadas, detecção e prevenção de intrusão, aceleração de aplicativos e muito mais, tudo isso sem a necessidade de incluir hardwares especiais.
	</p>

	<p>É possível que estes VNFs sejam fornecidos por um ou mais provedores. Cada VNF possui alguns metadados associados a ele que descrevem suas características essenciais. O serviço de rede real é composto pelo conjunto de todos os fluxos de pacotes que atravessam o plano de encaminhamento NFV e físico.
	</p>

	<h5>NFVI</h5>

	<p>Definimos “Network Function Virtualization Infrastructure” (NFVI) como o conjunto de componentes de Software e Hardware na qual podemos implementar, executar e gerenciar uma função de rede (NF). A NFVI pode ser composta de múltiplos pontos de presença (NFVI-PoP), que são localidades onde uma NF é implementada ou como função física (PNF) ou virtual de rede (VNF). A rede que provê conectividade entre esses pontos também é de responsabilidade do design de projeto da NFVI.
	</p>

	<p>A camada de hardware no NFVI inclui recursos de processamento, armazenamento e conectividade através da camada de virtualização. É essencial que esses recursos de hardware sejam de propósito geral, ou COTS (Commercial off-the-shelf). Interconectando esses recursos, há dois tipos de redes: NFVI-PoP e as redes de transporte que os interconectam.
	</p>

	<p>Outra importante camada em NFVU é a de virtualização, que abstraí os recursos de hardware e desacopla o software garantindo independência do hardware a ser utilizado. O desacoplamento, em geral, é possível com hypervisors que são uma das soluções mais atuais para tal camada. O VMWare, por exemplo, que permite a execução de diversas máquinas virtuais em máquinas de propósitos gerais. Para conectividade, a virtualização de recursos de redes inclui técnicas como: VxLANs e OpenFlow.
	</p>

	<h5>Hypervisor</h5>

	<p>Uma das principais características do NFV é o desacoplamento das funções de rede dos hardwares especializados, possibilitando o uso de hardwares de propósito geral. Para obter essa vantagem, é necessário criar uma camada de virtualização na infraestrutura de NFV através do particionamento lógico dos recursos (slicing) entre as funções de rede virtuais. Este desacoplamento dos recursos de computação e armazenamento do software é realizado por meio de hypervisors.
	</p>

	<p>Sucintamente, um hypervisor é um programa que provém uma camada de abstração para o hardware de rede, permitindo execução de diversas máquinas virtuais em hardware de propósito geral no contexto de NFV.
	</p>

	<img src="src/components/VirtualizationTab/image09.png" alt="">

	<p>Mesmo não existindo um padrão para a abstração em NFV, o uso de hypervisors é bem comum. Por exemplo, uma função de rede virtual pode ser executada em uma ou mais máquinas virtuais. Para uma execução eficiente, deve haver conectividade entre as máquinas virtuais. Através dos hypervisors de NFV, é possível criar uma permissividade de acesso direto às funções de rede ou uma comunicação direta entre máquinas virtuais. Várias técnicas são implementadas neste âmbito, tais como VxLANs (Virtual Extensible Local Area Network), NVGRE (Network Virtualisation using Generic Routing Encapsulation) e OpenFlow.
	</p>

	<h5>Orquestrador</h5>

	<p>Uma vantagem de usar NFV é a entrega de serviços de hardware industrial por meio de software. Este modelo entrega serviços mais rápidos e com mais flexibilidade. Porém, isso gera uma demanda considerável por recursos virtuais, necessitando de um gerenciamento de alto nível para manter a funcionalidade da rede. Este gerenciamento é chamado de orquestração.
	</p>

	<p>Para tanto, a orquestração se constrói com base no modelo dos hypervisor e outros softwares próprios para gerenciamento (vSphere, OpenStack, CloudStack). Assim, têm-se o Orquestrador de NFV, responsável por orquestrar e gerenciar de forma ampla os recursos de NFV (infraestrutura e software). Ele possui o controle e a visibilidade da topologia de serviços e de todas as funções de rede virtualizadas sendo executadas dentro da infraestrutura de NFV.
	</p>

	<img src="src/components/VirtualizationTab/image08.png" alt="">

	<p>Esse sistema cuida para que as máquinas virtuais e as funções de rede estejam otimizadas em suas funcionalidades e de acordo com o ambiente em que se encontram. Um desafio apresentado por isso é a migração dessas funções, requerendo a manutenção de seu estado durante sua realocação, replicação oi qualquer tipo de gerenciamento de escalabilidade. Agregadas a estes serviços estão as tarefas de detecção, diagnóstico e recuperação de falhas. Cabe ao orquestrador verificar a integridade operacional da infraestrutura de NFV em todos os níveis de aplicação.
	</p>

  </div>
</section>
</template>