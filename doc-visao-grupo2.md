# Documento de Visão – Marketplace de Produtos Alimentícios Diretos do Produtor
Grupo 2  
Versão 2.0  

---

## 1. Introdução

### 1.1. Contexto do Problema
Atualmente, pequenos produtores rurais enfrentam dificuldades para comercializar seus produtos diretamente ao consumidor. A maioria depende de intermediários ou vendas em feiras locais, o que reduz a margem de lucro e limita o alcance de clientes.  

Do outro lado, os consumidores buscam praticidade, preços justos e maior transparência sobre a origem dos alimentos. O modelo atual gera insatisfação tanto para produtores (pela limitação de vendas) quanto para consumidores (pelo custo e dificuldade de acesso a alimentos frescos).  

### 1.2. Motivação e Objetivos
O projeto visa criar uma plataforma digital (marketplace) que conecte diretamente produtores e consumidores, oferecendo um canal de vendas justo e eficiente.  

Os objetivos principais são:  
- Aumentar a visibilidade dos produtores locais.  
- Garantir mais praticidade na compra de alimentos frescos.  
- Oferecer preços competitivos ao consumidor, reduzindo a dependência de intermediários.  
- Automatizar processos como cálculo de frete, pagamentos e relatórios.  

---

## 2. Descrição Geral

### 2.1. Perspectiva do Produto
O sistema funcionará como um marketplace web/mobile que permitirá a interação entre **produtores**, **consumidores**, **entregadores** e **administradores**.  

- **Para o produtor:** será um canal de vendas com gerenciamento de produtos, preços e pedidos, além de relatórios de desempenho.  
- **Para o consumidor:** será uma vitrine digital de produtos locais com opção de compra simplificada e pagamento integrado.  
- **Para o entregador:** o sistema poderá sugerir rotas e organizar pedidos para otimizar entregas.  
- **Para o administrador:** será possível gerenciar usuários, monitorar atividades e manter a governança da plataforma.  

### 2.2. Usuários Principais (Atores)
- **Produtor:** cadastra produtos, ajusta preços, gerencia pedidos e acompanha relatórios.  
- **Consumidor:** visualiza produtos, realiza pedidos, efetua pagamentos e avalia produtores.  
- **Entregador:** consulta pedidos atribuídos, acessa rotas e atualiza status de entregas.  
- **Administrador:** gerencia usuários, monitora o sistema e gera relatórios globais.  

### 2.3. Funcionalidades de Alto Nível
O sistema permitirá que os usuários realizem as seguintes ações:  
- Cadastro e autenticação de usuários (produtor, consumidor, entregador, administrador).  
- Cadastro e gerenciamento de produtos (fotos, descrições, preços e disponibilidade).  
- Realização de pedidos com cálculo de frete automático.  
- Pagamento online integrado.  
- Sistema de avaliação (nota + comentários).  
- Relatórios de vendas para produtores e relatórios gerais para administradores.  
- Consultas a rotas e atualização de status por parte dos entregadores.  

---

## 3. Requisitos

- **RF01 - Cadastro de Usuários:** O sistema deve permitir o cadastro de produtores, consumidores, entregadores e administradores.  
- **RF02 - Gestão de Produtos:** O produtor deve poder cadastrar, editar e excluir produtos com fotos, descrições e preços.  
- **RF03 - Catálogo de Produtos:** O consumidor deve poder visualizar a lista de produtos disponíveis, com filtros e busca.  
- **RF04 - Realização de Pedidos:** O consumidor deve poder selecionar produtos, calcular o frete e finalizar o pedido.  
- **RF05 - Pagamento Integrado:** O sistema deve oferecer pagamento digital (cartão, Pix, boleto).  
- **RF06 - Avaliações:** O consumidor deve poder avaliar o produtor após a compra (1 a 5 estrelas + comentário).  
- **RF07 - Relatórios:** O produtor deve ter acesso a relatórios de vendas e o administrador a relatórios globais.  
- **RF08 - Gestão de Entregas:** O entregador deve receber pedidos, consultar rotas e atualizar status de entregas.  
- **RF09 - Administração do Sistema:** O administrador deve poder gerenciar usuários e categorias de produtos.  

---

## 4. Prioridades para o MVP (Minimum Viable Product)

Com base na entrevista, a primeira versão do sistema (MVP) deve conter:  
- Cadastro de produtores e consumidores.  
- Catálogo de produtos com fotos e descrições.  
- Realização de pedidos com cálculo de frete.  
- Pagamento digital básico.  
- Histórico de pedidos para produtor e consumidor.  

Funcionalidades como integração com entregadores, relatórios avançados e sistema de avaliação podem ser implementadas em versões futuras.  

---

## 5. Restrições e Premissas

### 5.1. Restrições
- O sistema deve estar disponível para acesso via navegador e aplicativo mobile.  
- Deve armazenar dados em nuvem para garantir disponibilidade e escalabilidade.  
- A primeira versão não incluirá integração completa de logística de entrega.  

### 5.2. Premissas
- Os produtores e consumidores possuem acesso à internet e dispositivos móveis.  
- Os usuários estão dispostos a utilizar a plataforma para centralizar compras e vendas.  
- O sistema deve ser intuitivo e acessível para pessoas com baixo nível de letramento digital.  

---

## 6. Critérios de Sucesso
O sucesso do projeto será medido pelos seguintes critérios:  
- Pelo menos 70% dos produtores cadastrados realizarem vendas na plataforma nos três primeiros meses.  
- Pelo menos 80% de satisfação dos consumidores (com base nas avaliações no app).  
- Redução da dependência de intermediários para os produtores participantes.  
- Aumento do alcance dos produtores em pelo menos 40% comparado às vendas locais.  
