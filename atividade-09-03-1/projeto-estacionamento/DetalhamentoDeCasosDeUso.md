# Caso de Uso: Registrar Entrada de Veículo

**Escopo:**  

Funcionalidades Check-in  

**Propósito:**  
Este caso de uso é responsável pelo registro dos dados importantes sobre o check-in de um cliente.  

**Ator:**  
Atendente ou Gerente

**Pré-condições:**  
O atendente deve estar conectado ao sistema de controle de estacionamento.  

**Pós-condições:**  
Os dados de horário de entrada e placa do veículo são armazenados e uma vaga é alocada ao cliente.  

## Fluxo de Eventos Normal  
- O atendente do estacionamento insere a placa do veículo fazendo check-in.  
- O sistema automaticamente verifica a disponibilidade de vagas e, se possível, registra que o cliente está ocupando uma das vagas juntamente ao horário de entrada.  

## Fluxo de Eventos de Exceção  
- **Não haviam vagas disponíveis:** Se não há vagas disponíveis, o sistema informa ao atendente sobre a lotação do estacionamento juntamente com uma estimativa de tempo para uma vaga ser desocupa da, calculada automaticamente com base na média de tempo de permanência das vagas.  
- O check-in é cancelado.  

**Requisitos Relacionados:**  
RF1, RF2, RF3, RF4, RF5  
RNF1, RNF2, RNF3, RNF4, RNF5, RNF6, RNF7  

**Classes:**  
CheckIn, Vagas, GerenciadorDeVagas, Cliente, HistoricoDabatabase  

---

# Caso de Uso: Registrar Saída de Veículo  

**Escopo:**  
Funcionalidades Check-out  

**Propósito:**  
Este caso de uso é responsável pelo registro do check-out de um cliente.  

**Ator:**  
Atendente ou Gerente

**Pré-condições:**  
Deve ter sido feito o registro do check-in do veículo.  

**Pós-condições:**  
O tempo total de permanência e o valor de cobrança são calculados. A efetuação do pagamento é registrada e uma vaga é liberada.  

## Fluxo de Eventos Normal  
- O atendente do estacionamento seleciona o cliente que está fazendo check-out.  
- O sistema retorna o tempo total de permanência e o valor de cobrança.  
- Após a cobrança, o atendente confirma que o check-out foi efetuado.  
- A vaga alocada ao cliente em questão é liberada e o check-out é registrado.  

## Fluxo de Eventos de Exceção  
- **O tempo de permanência mínimo para cobrança não foi atingido:** O atendente é informado que não é necessário realizar cobrança.  
- O atendente confirma que o check-out foi efetuado.  
- A vaga alocada ao cliente em questão é liberada e o check-out é registrado.  

**Requisitos Relacionados:**  
RF1, RF2, RF3, RF4, RF5  
RNF1, RNF2, RNF3, RNF4, RNF5, RNF6, RNF7  

**Classes:**  
CheckIn, Vagas, GerenciadorDeVagas, Cliente, HistoricoDabatabase  

---

# Caso de Uso: Gerenciar Vagas  

**Escopo:**  
Funcionalidades Gerenciamento  

**Propósito:**  
Este caso de uso é responsável pela administração das vagas disponíveis no estacionamento, permitindo ao atendente atualizar o status de ocupação e realizar bloqueios ou liberações manuais.  

**Ator:**  
Atendente ou Gerente

**Pré-condições:**  
O atendente deve estar conectado ao sistema de controle de estacionamento.  

**Pós-condições:**  
O status das vagas é atualizado no sistema, garantindo informações consistentes para check-in e check-out.  

## Fluxo de Eventos Normal  
- O atendente acessa a funcionalidade de gerenciamento de vagas.  
- O sistema exibe a lista de vagas e seu status atual (ocupada, livre, reservada, bloqueada).  
- O atendente pode alterar o status de uma vaga ou consultar informações sobre ela.  

## Fluxo de Eventos de Exceção  
- **Falha de sincronização:** Caso haja inconsistências no status das vagas, o sistema exibe uma mensagem de alerta e solicita que o atendente atualize as informações manualmente.  

**Requisitos Relacionados:**  
RF3, RF5
RNF1, RNF2, RNF5

**Classes:**  
Vagas, GerenciadorDeVagas, CheckIn, CheckOut  

---

# Caso de Uso: Visualizar Mapa do Estacionamento  

**Escopo:**  
Funcionalidades Gerenciamento  

**Propósito:**  
Este caso de uso permite ao atendente acompanhar em tempo real a ocupação das vagas no estacionamento por meio de um mapa visual.  

**Ator:**  
Atendente ou Gerente

**Pré-condições:**  
O sistema deve estar conectado ao banco de dados de vagas e com atualização em tempo real habilitada.  

**Pós-condições:**  
O atendente tem uma visão geral da ocupação das vagas e pode utilizá-la para orientar clientes.  

## Fluxo de Eventos Normal  
- O atendente acessa a função de mapa do estacionamento.  
- O sistema apresenta uma visualização gráfica das vagas indicando seu status (livre, ocupada, reservada).  

## Fluxo de Eventos de Exceção  
- **Falha na atualização em tempo real:** Caso o mapa não consiga atualizar as vagas, o sistema informa que os dados exibidos podem estar defasados.  

**Requisitos Relacionados:**  
RF3, RF5
RNF1, RNF2, RNF5  

**Classes:**  
MapaEstacionamento, Vagas, GerenciadorDeVagas  

---

# Caso de Uso: Consultar Histórico de Veículos  

**Escopo:**  
Funcionalidades Gerenciamento  

**Propósito:**  
Este caso de uso permite consultar registros de entradas e saídas anteriores de veículos no estacionamento.  

**Ator:**  
Atendente ou Gerente

**Pré-condições:**  
O veículo deve ter registros prévios no sistema.  

**Pós-condições:**  
As informações históricas são exibidas, podendo ser filtradas por período, placa ou cliente.  

## Fluxo de Eventos Normal  
- O atendente insere critérios de busca (placa, nome do cliente ou intervalo de datas).  
- O sistema exibe a lista de entradas e saídas correspondentes.  

## Fluxo de Eventos de Exceção  
- **Nenhum registro encontrado:** O sistema informa que não há registros correspondentes aos critérios informados.  

**Requisitos Relacionados:**  
RF3, RF5
RNF1, RNF2, RNF5  

**Classes:**  
HistoricoDatabase, Cliente, CheckIn, CheckOut  

---

# Caso de Uso: Gerar Relatórios  

**Escopo:**  
Funcionalidades Gerenciamento  

**Propósito:**  
Este caso de uso é responsável pela geração de relatórios gerenciais sobre ocupação, faturamento e desempenho do estacionamento.  

**Ator:**  
Gerente  

**Pré-condições:**  
O gerente deve estar autenticado no sistema com permissões de acesso administrativo.  

**Pós-condições:**  
Um relatório é gerado e disponibilizado em tela ou exportado em formato digital.  

## Fluxo de Eventos Normal  
- O gerente seleciona o tipo de relatório desejado (ocupação diária, faturamento, tempo médio de permanência).  
- O sistema processa as informações e gera o relatório solicitado.  

## Fluxo de Eventos de Exceção  
- **Dados insuficientes:** Se não houver dados suficientes para gerar o relatório, o sistema exibe mensagem explicativa.  

**Requisitos Relacionados:**  
RF3, RF5
RNF1, RNF2, RNF5  

**Classes:**  
Relatorio, HistoricoDatabase, GerenciadorDeVagas, Cliente  

---

# Caso de Uso: Receber Alertas de Lotação  

**Escopo:**  
Funcionalidades Gerenciamento  

**Propósito:**  
Este caso de uso é responsável por notificar o gerente sobre a lotação do estacionamento ou eventos críticos relacionados à disponibilidade de vagas.  

**Ator:**  
Gerente  

**Pré-condições:**  
O sistema deve monitorar em tempo real a ocupação do estacionamento.  

**Pós-condições:**  
O gerente é notificado por meio do painel do sistema ou por alerta externo (ex.: e-mail, aplicativo).  

## Fluxo de Eventos Normal  
- O sistema identifica que a taxa de ocupação ultrapassou um limite configurado.  
- O sistema gera automaticamente um alerta e envia para o gerente.  

## Fluxo de Eventos de Exceção  
- **Falha de notificação:** Se não for possível enviar a notificação, o sistema registra o evento e apresenta o alerta em log.  

**Requisitos Relacionados:**  
RF3, RF5
RNF3, RNF5  

**Classes:**  
GerenciadorDeAlertas, Gerente, Vagas  

---

# Resumo dos Casos de Uso

| Nome                         | Ator       | Escopo                     | Propósito (resumo)                                                                 |
|------------------------------|------------|-----------------------------|-----------------------------------------------------------------------------------|
| Registrar Entrada de Veículo | Atendente Gerente | Funcionalidades Check-in    | Registrar check-in do cliente, placa e horário de entrada, alocando vaga disponível. |
| Registrar Saída de Veículo   | Atendente Gerente | Funcionalidades Check-out   | Registrar check-out, calcular tempo e valor, confirmar pagamento e liberar vaga.   |
| Gerenciar Vagas              | Atendente Gerente | Funcionalidades Gerenciamento | Atualizar manualmente status das vagas (livre, ocupada, reservada, bloqueada).     |
| Visualizar Mapa do Estacionamento | Atendente Gerente | Funcionalidades Gerenciamento | Mostrar mapa visual em tempo real da ocupação de vagas.                            |
| Consultar Histórico de Veículos | Atendente Gerente | Funcionalidades Gerenciamento | Consultar registros de entradas/saídas por placa, cliente ou período.              |
| Gerar Relatórios             | Gerente    | Funcionalidades Gerenciamento | Gerar relatórios sobre ocupação, faturamento e desempenho.                         |
| Receber Alertas de Lotação   | Gerente    | Funcionalidades Gerenciamento | Notificar gerente sobre lotação ou eventos críticos de disponibilidade de vagas.   |
