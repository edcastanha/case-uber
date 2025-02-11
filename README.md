# case-system-design-uber

[Esboço Inicial - C4 Model](./design/img]/C4Model.png)

# Desafio de System Design do Uber

O objetivo deste desafio é projetar um sistema que atenda aos seguintes requisitos de engenharia, detalhando o que será abordado e o que está fora do escopo.

## Requisitos de Engenharia

### Requisitos Funcionais
* O passageiro deve poder solicitar uma nova corrida informando uma localização de origem e um destino, obtendo o valor estimado da corrida.
* O passageiro pode confirmar o início da corrida com base na solicitação anterior, onde ele já possui o valor calculado.
* O motorista poderá receber a solicitação de corrida e optar por aceitá-la ou recusá-la.
** Se aceitar, ele buscará o passageiro na localização de origem e o levará ao destino final.
** Se recusar, a corrida será disponibilizada para outro motorista na mesma região.

#### Não será abordado:
* Sistema de avaliação de motoristas e passageiros (nota de 5 estrelas).
* Categorização de tipos de veículo.
* Funcionalidades avançadas, como:
** Mudança de rota durante a corrida com recálculo do valor.
** Divisão de pagamento com múltiplos passageiros.

### Requisitos Não Funcionais
* O sistema deve localizar motoristas na região em menos de dois minutos; caso contrário, a solicitação deve ser cancelada.
* O sistema deve permitir que o passageiro acompanhe a movimentação do motorista em tempo real no mapa, mesmo que algumas atualizações possam apresentar um leve atraso para garantir disponibilidade.
* Para garantir consistência, o sistema deve evitar que um motorista aceite mais de uma corrida ao mesmo tempo, mesmo que isso signifique uma indisponibilidade temporária em casos críticos.
* Métricas importantes devem ser definidas para monitorar a disponibilidade, como tempo de resposta, uso de recursos computacionais, latência e taxa de falhas.
* O sistema deve operar de forma assíncrona, sempre que possível, para garantir resiliência e otimização de recursos.
* Sistema deve enviar notificações para o motorista e o passageiro sobre a corrida e a localização das partes envolvidas.

#### Não será abordado:
* Implementação de observabilidade completa (logs detalhados e tracing) – apenas métricas básicas serão consideradas.
* Processo de entrega de software.
* Detalhes de infraestrutura (como uso de Kubernetes).
* Procedimentos de recuperação em caso de falhas.

## Tarefas para Completar o System Design
* Identificar as principais entidades do sistema e suas relações.
* Estimar a capacidade necessária em termos de usuários simultâneos e requisições por segundo.
* Definir o design da API de alto nível com os principais endpoints e métodos.
* Criar o diagrama visual com as interações dos componentes do sistema.

! Considerar perguntas complexas e validar sua solução com respostas sobre escolha de banco de dados e estratégias de escalabilidade horizontal, mensageria, entre outros.
