# Diagramas de Casos de Uso — PETCONNECT

---

## **Visão Global**

O diagrama global consolida os principais **atores** e **fluxos** do sistema **PETCONNECT**.  
Ele apresenta de forma clara os atores centrais — **Dono de Pet**, **Profissional/Vendedor** e **Administrador** — além dos sistemas externos envolvidos (**Pagamento** e **Logística**).  

Os **casos de uso principais** incluem:  
- Cadastro e Login  
- Gerenciamento de Perfil  
- Transações  
- Pagamentos  
- Agenda  
- Avaliações  

As relações `<<include>>` e `<<extend>>` representam, respectivamente, **dependências obrigatórias** e **fluxos opcionais**.  
O objetivo é oferecer uma visão geral rápida e organizada do sistema, sem detalhar cada módulo em profundidade.

![Diagrama Global do PETCONNECT](https://github.com/ps-es-2025-2/geral/blob/grupo4/atividade-09-03-1/projeto-marketplace-de-pets/DiagramaGlobalPet.png?raw=true)

---

## **Módulo de Gestão de Contas**

Este diagrama detalha o gerenciamento de contas na plataforma.  
Ele evidencia a **generalização de atores**, mostrando que **Dono de Pet** e **Profissional/Vendedor** herdam funcionalidades do ator genérico **Usuário**.  

O caso de uso **Validar Perfil de Profissional** aparece como uma extensão do **Cadastro**, reforçando o papel do **Administrador** no processo de validação.

![Diagrama de Gestão de Contas](https://github.com/ps-es-2025-2/geral/blob/grupo4/atividade-09-03-1/projeto-marketplace-de-pets/DiagramaGestaoContas.png?raw=true)

---

## **Módulo de Marketplace**

Este diagrama foca no fluxo principal de transações.  
O uso de `<<include>>` mostra que, para **Agendar Serviços** ou **Comprar Produtos**, é obrigatório realizar **Login** e **Pagamento**.  

Também é destacada a integração com sistemas externos de **Pagamento** e **Logística**, garantindo a confirmação das transações e a entrega eficiente dos produtos.

![Diagrama de Marketplace](https://github.com/ps-es-2025-2/geral/blob/grupo4/atividade-09-03-1/projeto-marketplace-de-pets/DiagramaMarketplace.png?raw=true)

---

## **Módulo do Profissional**

Este diagrama concentra-se nas funcionalidades exclusivas de profissionais e vendedores.  
O caso de uso **Gerenciar Perfil Profissional** aparece como especialização do genérico **Gerenciar Perfil**.  

Além disso, o diagrama contempla o gerenciamento de:  
- Serviços e Produtos  
- Agenda de Pedidos  

Dessa forma, deixa claro o papel do profissional dentro da plataforma.

![Diagrama do Profissional](https://github.com/ps-es-2025-2/geral/blob/grupo4/atividade-09-03-1/projeto-marketplace-de-pets/DiagramaProfissional.png?raw=true)

---

## **Módulo de Avaliação e Conteúdo**

Este diagrama aborda funcionalidades de **engajamento** e **confiança**.  
Usuários podem **Consultar Avaliações** e **Acessar Conteúdos Informativos**, enquanto apenas **Donos de Pets autenticados** podem **Registrar Avaliações**.  

O uso de `<<include>>` com **Login** reforça a exigência de autenticação, assegurando a confiabilidade das informações.

![Diagrama de Avaliação e Conteúdo](https://github.com/ps-es-2025-2/geral/blob/grupo4/atividade-09-03-1/projeto-marketplace-de-pets/DiagramaAvaliacao.png?raw=true)

---

## **Módulo de Administração**

Este diagrama evidencia as responsabilidades do **Administrador** na plataforma.  
O fluxo **Validar Perfil de Profissional** aparece como extensão (`<<extend>>`) do **Cadastro**, demonstrando sua natureza opcional.  

Também é mostrado o gerenciamento de **Conteúdo Informativo**, reforçando a importância do administrador na qualidade e credibilidade do sistema.

![Diagrama de Administração](https://github.com/ps-es-2025-2/geral/blob/grupo4/atividade-09-03-1/projeto-marketplace-de-pets/DiagramaAdmin.png?raw=true)
