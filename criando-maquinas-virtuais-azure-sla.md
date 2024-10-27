# Microsoft Azure - 
##   Criando máquinas Virtuais na Azure

### Resumo
Nesse Laboratório foi abordado sobre SLA ( Service Level Agreement) termo no qual trata sobre o tempo de disponibilidade de aplicações e serviços entre o provedor Azure e seus clientes com a abordagem da criação de uma máquina virtual em mais de uma zona de disponibilidade.

Abaixo temos um recorte do site da Microsoft para disponibilidade um conjunto de máquina virtual:
> ## *Conjuntos de Disponibilidade*
> *Um  conjunto de disponibilidade  é um agrupamento lógico de VMs que permite que o Azure entenda como o seu aplicativo foi criado para fornecer redundância e disponibilidade. Recomenda-se que duas ou mais VMs sejam criadas dentro de um conjunto de disponibilidade para fornecer um aplicativo altamente disponível e para atender o  SLA de 99,95% do Azure. Não há nenhum custo para o conjunto de disponibilidade em si, você paga apenas por cada instância de VM que criar.*

### **Zonas de Disponibilidade**
Zona de disponibilidade é uma localização física onde esta situado um Datacenter da Azure.
As zonas de disponibilidades estão situadas em uma **REGIÃO** e cada região tem pelos menos 3 zonas distantes uma das outras. A exemplo caso ocorra um desastre geológico / indisponibilidade na zona 1 , os serviços seguem mantidos normalmente nas zonas 2 e 3, garantindo assim o SLA acordado.

<img src="https://learn.microsoft.com/pt-br/azure/reliability/media/cross-region-replication.png" width="500px">

Os SLAs estão atrelados e ou condicionados aos tipos de serviços e aplicações utilizadas pelo cliente onde tais itens devem estar em conformidade com as regras e ou documentação de implantação disponibilizado pelo provedor.

Abaixo na tabela temos uma visão geral sobre os níveis de SLA :white_check_mark:
|Objetivo | Não conformidade por semana | Não conformidade por mês | Não conformidade por ano |
|--------|-------------------------|---------------------|---------------------|
|	99%		|	1,68 hora	|	7.20 horas		|	3,65 dias	|
|	99,90%	|	10.10 minutos	|	43.20 minutos|	8,76 horas	|	|	99,95%	|	5 minutos	|	21.60 minutos	|	4,38 horas	|
|	99,99%	|	1,01 minuto	|	4,32 minutos	|	52,56 minutos|
|	99,999%	|	6 segundos	|	25,90 segundos	|	5,26 minutos|

- Quanto maior a precisão dos dígitos após a vírgula, menor é o tempo de indisponibilidade.
- Quanto maior o número de zonas de replicação dos serviços ou aplicações menor o tempo de indisponibilidade.

Portanto no momento de implantação a não observância das regras do provedor pode implicar na perda do direito de cumprimento do SLA, uma vez que o cliente é o responsável direito pelo provisionamento dos serviços.
