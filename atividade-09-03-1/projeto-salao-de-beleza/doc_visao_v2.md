# Documento de Visão – Aplicativo Beleza & Estilo

## Grupo 1
| Aluno | Github |
|-------------|-------------|
|Gabriel Freitas dos Reis | GabrielFRails
|Gabriel Rodrigues Silva | Gabriellrs
|Laura Martins Vieira Gonçalves | lauramvg1821
|Léia Santos Costa | Leia27
|Tallya Jesus Sousa Barbosa | tallya01

**Versão 1.0**

## 1. Introdução

### 1.1. Contexto do Problema
Atualmente, o salão "Beleza & Estilo" gerencia seus agendamentos manualmente por meio do WhatsApp e de ligações telefônicas. Esse processo é ineficiente, consome muito tempo da proprietária, Maria, e resulta em problemas como agendamentos duplicados para o mesmo horário. A falta de um sistema centralizado dificulta a visualização do histórico de serviços dos clientes e a análise do desempenho do negócio.

### 1.2. Motivação e Objetivos
O projeto visa desenvolver um aplicativo móvel para automatizar e otimizar o processo de agendamento de serviços. O objetivo principal é oferecer uma plataforma onde os clientes possam visualizar os horários disponíveis e agendar serviços de forma autônoma, reduzindo a carga de trabalho manual da equipe e eliminando conflitos de agenda.

## 2. Descrição Geral

### 2.1. Perspectiva do Produto
O "App Beleza & Estilo" será um aplicativo móvel (para Android e iOS) que conectará os clientes ao salão. Para os clientes, funcionará como uma ferramenta de autoatendimento para agendamentos. Para a proprietária e a equipe, servirá como um painel de gerenciamento para visualizar a agenda diária, gerenciar clientes e extrair relatórios básicos de desempenho.

### 2.2. Usuários Principais (Atores)
* **Cliente:** Pessoa que busca agendar um serviço no salão. É o usuário final do aplicativo. O público-alvo principal são mulheres entre 20 e 50 anos, mas a interface deve ser simples para todos os públicos.
* **Proprietária (Maria):** Responsável por gerenciar o salão, visualizar relatórios de atendimentos, cadastrar serviços/preços e enviar promoções.
* **Profissional:** Membro da equipe do salão que precisa visualizar seus agendamentos do dia.

### 2.3. Funcionalidades de Alto Nível
O sistema permitirá que os usuários realizem as seguintes ações:
* Visualizar a lista de serviços oferecidos pelo salão, com seus respectivos preços.
* Consultar a agenda e os horários disponíveis para cada profissional.
* Realizar o agendamento de um ou mais serviços.
* Cadastrar-se de forma simples (nome e telefone).
* Receber notificações de confirmação e lembretes de agendamento.
* A proprietária poderá visualizar um resumo semanal de atendimentos.

## 3. Requisitos de Alto Nível (Features)

* **RF01 - Gestão de Serviços:** A proprietária deve poder cadastrar os serviços oferecidos, seus preços e as profissionais que os realizam.
* **RF02 - Agendamento Online:** O cliente deve poder selecionar um serviço, uma profissional e um horário disponível para realizar o agendamento.
* **RF03 - Cadastro de Clientes:** O cliente deve poder realizar um cadastro simples (nome e telefone) para utilizar o sistema. O sistema deve armazenar um histórico de serviços realizados por cliente.
* **RF04 - Sistema de Notificações:** O sistema deve enviar notificações de confirmação (no momento do agendamento) e lembretes (próximo à data/hora) para o cliente. A equipe também deve ser notificada sobre novos agendamentos.
* **RF05 - Geração de Relatórios:** A proprietária deve ter acesso a um painel com um resumo semanal, mostrando a quantidade de atendimentos e os serviços mais procurados.
* **RF06 - Personalização da Identidade Visual:** O aplicativo deve conter a logo e as cores do salão "Beleza & Estilo".

## 4. Prioridades para o MVP (Minimum Viable Product)
Com base na entrevista, a primeira versão do aplicativo (MVP) deve focar nas seguintes funcionalidades essenciais:
1.  Lista de serviços com preços.
2.  Visualização da agenda com horários disponíveis.
3.  Funcionalidade de agendamento pelo aplicativo.
4.  Cadastro simples de clientes.
5.  Envio de notificação de confirmação do horário.

Funcionalidades como pagamento online e login com redes sociais serão consideradas para versões futuras.

## 5. Restrições e Premissas

### 5.1. Restrições
* O sistema deve ser um aplicativo móvel compatível com as plataformas Android e iOS.
* A primeira versão não incluirá funcionalidade de pagamento dentro do aplicativo.
* O sistema de notificação inicial pode ser via WhatsApp ou notificações push do próprio app.

### 5.2. Premissas
* Assume-se que os clientes do salão possuem smartphones e estão dispostos a usar um aplicativo para agendamentos.
* O salão possui acesso à internet para sincronização dos dados do aplicativo.

## 6. Critérios de Sucesso
O sucesso do projeto será medido pelos seguintes critérios:
* Redução de 50% do tempo gasto pela proprietária com marcações manuais via WhatsApp e telefone.
  * Justificativa: ao implantar o aplicativo, será necessário um prazo para adesão das clientes do salão. Além disso, novas clientes precisarão conhecer e aderir ao aplicativo, e enquanto isso realizar os agendamentos ainda com a proprietária.
* Garantia de 100% de disponibilidade real para agendamentos feitos via app: O sistema não permitirá que um horário já ocupado (seja por agendamento via app ou manual) seja agendado novamente pelo aplicativo, eliminando conflitos de agendamento originados na plataforma.
   * Justificativa: Redução de 90% dos conflitos de agendamento manuais: Ao centralizar a visualização da agenda, a proprietária terá uma ferramenta confiável para consultar antes de realizar agendamentos manuais, minimizando erros.
* Aumento a partir de 40% na retenção de clientes ao oferecer uma forma mais prática e autônoma de agendamento.
  * Justificativa: o cliente terá acesso aos serviços, valores e à agenda de forma instantânea, sem a necessidade de esperar retorno da proprietária para realizar um agendamento. O aumento pode ser maior caso haja uma boa adesão ao app.
* Aumento de receita com o uso efetivo dos relatórios semanais para planejar promoções e entender a demanda de serviços.
  * Justificativa: os relatórios permitirão a elaboração de estratégias precisas para captação e retenção de clientes

