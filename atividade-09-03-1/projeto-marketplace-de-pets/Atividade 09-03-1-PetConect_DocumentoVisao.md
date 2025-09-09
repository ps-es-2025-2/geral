# 

**PETCONNECT – Marketplace de Serviços e Produtos Pet**

**Documento de Visão**

**Versão 1.0**

# 

| Histórico de Revisões |  |  |  |
| :---: | :---: | ----- | ----- |
| **Versão** | **Data** | **Descrição** | **Autor** |
| 1.0 | 07/09/2025 | Criação da versão inicial do documento com base na entrevista com o requisitante. | Daired Almeida Cruz(PMO) |
| 1.1 | 08/09/2025 | Revisão do documento para adequação com capacidade técnica da equipe e infraestrutura do stakeholder. | Filipe Paço(Arquiteto de Software) |
|  |  |  |  |

# 

**Sumário**

[1\. Introdução	4](#introdução)

[2\. Identificação do Projeto	4](#identificação-do-projeto)

[3\. Problema	4](#problema)

[4\. Usuários	5](#usuários)

[5\. Visão Geral do Produto	7](#visão-geral-do-produto)

[6\. Características do Produto	8](#características-do-produto)

[7\. Interface com Outros Sistemas	9](#interface-com-outros-sistemas)

[8\. Restrições Impostas	10](#restrições-impostas)

[9\. Precedência e Prioridade	10](#precedência-e-prioridade)

[10\. Requisitos de Documentação	10](#requisitos-de-documentação)

[11\. Anexos	11](#anexos)

[12\. Referências	11](#heading=h.bvdyv35jprvy)

[13\. Aprovações	12](#heading=h.w6pzvwo7cddv)

	**Documento de Visão**	

1. # **Introdução**

Este documento fornece uma visão geral do projeto de marketplace para o setor pet, o PETCONNECT. Ele tem como finalidade descrever o problema a ser resolvido, os usuários envolvidos, as funcionalidades e as restrições do sistema, servindo como guia para o desenvolvimento do projeto.

2. # **Identificação do Projeto**

| Projeto | PETCONNECT – Marketplace de Serviços e Produtos Pet  |
| :---- | :---- |
| **Requisitante** | Ricardo (Veterinário Empreendedor)  |
| **Gerente de Projetos** | Daired Almeida Cruz |

3. # **Problema**

Esta seção descreve o problema que o projeto visa solucionar, identificando os envolvidos e o escopo geral.

1. ## **Resumo do Negócio**

O mercado de cuidados para animais de estimação é vasto e fragmentado, com diversos profissionais e estabelecimentos (veterinários, pet shops, adestradores, creches) atuando de forma independente. Atualmente, os donos de pets enfrentam dificuldades para encontrar, comparar e contratar serviços ou comprar produtos em um único ambiente confiável.

2. ## **Problemas**

| O problema de | Falta de uma plataforma centralizada que conecte donos de pets a uma gama completa de profissionais, serviços e produtos do mercado pet. |
| :---- | :---- |
| **Afeta** | Donos de pets, veterinários, adestradores, cuidadores, creches, clínicas e pet shops. |
| **Cujo impacto é** | A dificuldade para donos de pets encontrarem serviços confiáveis, gerando perda de tempo em pesquisas dispersas. Para os profissionais, há uma barreira para alcançar novos clientes e gerenciar seus serviços de forma eficiente.  |
| **Benefícios de uma solução seriam** | Maior conveniência e confiança para os donos de pets, que poderão encontrar, agendar, pagar e avaliar serviços em um só lugar. Aumento da visibilidade e otimização da gestão para os profissionais e negócios do setor. |

4. #  **Usuários**

   1. ## **Resumo dos Usuários**

| Nome | Descrição | Responsabilidades |
| ----- | ----- | ----- |
| Dono de Pet (Cliente) | Pessoa que possui um ou mais animais de estimação e busca por serviços, produtos e informações de qualidade. | Buscar e filtrar profissionais, serviços e produtos. Agendar serviços e comprar produtos. Realizar o pagamento através da plataforma. Avaliar os serviços e produtos adquiridos. |
| Profissional/Vendedor Pet | Profissionais autônomos (veterinários, adestradores) e negócios (clínicas, pet shops) que oferecem seus serviços ou produtos no mercado.  | Realizar cadastro e validação de perfil na plataforma. Divulgar seus serviços e/ou produtos. Gerenciar agendamentos de pedidos recebidos. Receber os pagamentos por meio da plataforma. |

   2. ## **Ambiente do Usuário**

O sistema será uma plataforma web responsiva, acessível por meio de navegadores em desktops e dispositivos móveis. Inicialmente, não há restrições de hardware ou software específicas além da necessidade de acesso à internet. O sistema deverá interagir com aplicativos externos para processamento de pagamentos e logística. 

3. ## **Necessidades dos Interessados**

| Crítico | Requisitos essenciais ou o fracasso em sua implementação significa que o sistema não irá atender as necessidades do cliente. Imprescindível que seja atendido pelo sistema, condição fundamental para o sucesso do projeto.  |
| :---: | :---- |
| Importante | Requisitos importantes para a eficácia ou eficiência do sistema. Sua não implementação afeta a satisfação do usuário e/ou o valor agregado do produto. Afeta a satisfação do usuário significativamente, mas o não atendimento não determina o fracasso do projeto. |
| Útil | Requisitos úteis, porém menos críticos, sendo usados menos frequentemente. Não possui muito significado para a satisfação do usuário e pode deixar de ser atendida. |

| Necessidade | Prioridade | Preocupações | Solução Atual | Soluções Propostas |
| ----- | ----- | ----- | ----- | ----- |
| Dono de Pet necessita encontrar, agendar e pagar por diversos serviços e produtos em um único local confiável. | Crítico | Perda de tempo pesquisando em múltiplos sites e redes sociais. Insegurança ao contratar profissionais sem referências ou avaliações.  | Buscas no Google Redes sociais. Indicações de conhecidos.  | Marketplace centralizado com busca e filtros avançados. Perfis de profissionais verificados. Sistema de avaliação pública.   |
| Profissional/Vendedor Pet necessita de uma ferramenta para divulgar seu trabalho e gerenciar seus clientes e pagamentos.  | Crítico  | Dificuldade para alcançar um público maior. Falta de um sistema integrado para agendamentos e recebimentos.  | Sites próprios. Marketing em redes sociais. Controles manuais (planilhas, agenda).  | Perfil profissional com portfólio e descrição de serviços/produtos.  Painel de controle para gestão de pedidos, agenda e pagamentos. |
| Dono de Pet necessita de acesso a conteúdo informativo de qualidade sobre cuidados com animais.  | Importante  | Encontrar informações conflitantes ou de baixa credibilidade na internet.  | Blogs genéricos. Vídeos e postagens em redes sociais.  | Seção de conteúdo (artigos, dicas) criada e validada por profissionais da plataforma.  |

5. # **Visão Geral do Produto**

Esta seção descreve o produto que solucionará o problema, indicando suas principais capacidades para atender às necessidades dos usuários. 

1. ## **Perspectiva do Produto**

O PETCONNECT será uma plataforma web independente e autossuficiente.  Ele atuará como um intermediário entre clientes e prestadores de serviço/vendedores. Para seu funcionamento pleno, o sistema interagirá com sistemas externos, como gateways de pagamento e plataformas de logística.

2. ## **Resumo das Capacidades do Produto**

| Benefícios para o Cliente | Recursos do Sistema |
| ----- | ----- |
| Agilidade e confiança para encontrar e contratar os melhores serviços e produtos para seus pets.   | Sistema de busca e filtros para serviços, produtos e profissionais. Agendamento e pagamento online. Perfis verificados e sistema de avaliação com estrelas e comentários.  |
| Maior visibilidade e gestão simplificada para profissionais e negócios do setor pet. | Criação de perfis públicos para divulgação de portfólio. Painel administrativo para gerenciamento de pedidos, agendamentos e recebíveis. Monetização por taxa de transação, com possibilidade de planos premium no futuro. |
| Acesso a informações confiáveis para o cuidado com os animais de estimação. | Uma área de conteúdo com artigos, dicas e vídeos produzidos por especialistas da área.  |

6. # **Características do Produto**

## A seguir, são listadas as principais características que o sistema deverá fornecer. 

1. ## **Gestão de Perfis e Verificação** 

## O sistema deve permitir que profissionais e vendedores criem perfis detalhados e deve incluir um processo de validação de documentos para garantir a transparência e a segurança. 

2. ## **Marketplace de Serviços e Produtos** 

## O sistema deve permitir que os clientes busquem, comparem, agendem ou comprem serviços e produtos diretamente pela plataforma. Posteriormente será esclarecido com o stakeholder mais detalhes sobre o agendamento como a necessidade de possuir notificações via email ou não.

3. ## **Sistema de Pagamento Integrado** 

## O sistema deve processar pagamentos online para todas as transações, garantindo o repasse aos vendedores e a cobrança de uma taxa de serviço. 

Obs.: Esse ponto deve ser alterado a depender da contratação de um dev com experiência em meios de pagamento.

4. ## **Sistema de Avaliação** 

## O sistema deve permitir que clientes avaliem os serviços e produtos adquiridos por meio de notas (estrelas) e comentários. 

5. ## **Plataforma de Conteúdo** 

## O sistema deve possuir uma área para a publicação de artigos e dicas sobre cuidados com animais, a fim de engajar e educar os usuários. 

Obs: Alinhar com gestor de projetos a capacidade da infra do stakeholder, creio que não suportará e iremos novamente sugerir hospedagem aws.

6. ## **Integração Logística** 

## O sistema deve ser capaz de se integrar a parceiros logísticos para gerenciar a entrega de produtos vendidos na plataforma.

7. # **Interface com Outros Sistemas**

A plataforma PETCONNECT (Sistema A) precisará interagir com os seguintes sistemas externos (Sistema B):

| Sistema | Descrição | Tipo da Integração |
| ----- | ----- | ----- |
| Gateway de Pagamento | Processar as transações de compra de produtos e agendamento de serviços, gerenciando os pagamentos dos clientes e os repasses aos vendedores. | Tipo 2 e Tipo 4 |
| Plataforma de Logística | Realizar o cálculo de frete para a entrega de produtos e coordenar o envio dos pedidos. | Tipo 1 e Tipo 3 |

**Sistema A**: Sistema objeto desse documento de escopo preliminar.  
**Sistema B**: Sistema a se integrar com o sistema A  
Tipo 1: Sistema A consulta dados/informações no sistema B;  
Tipo 2 : Sistema A atualiza dados/informações no sistema B;  
Tipo 3 : Sistema A gera dados/informações para processamento no sistema B;  
Tipo 4 : Sistema A processa dados/informações gerado por B.

8. # **Restrições Impostas**

   1. ## **Tecnologia:** 

## O produto deve ser desenvolvido inicialmente como um site com design responsivo, compatível com os principais navegadores de mercado, com previsão para uma versão mobile no futuro.

2. ## **Prazos e Custos:** 

## O projeto deve ser desenvolvido considerando um orçamento limitado, típico de um negócio empreendedor em estágio inicial. Os prazos serão definidos em fases para permitir um lançamento rápido das funcionalidades essenciais (MVP). 

9. # **Precedência e Prioridade**

As características do sistema serão desenvolvidas com a seguinte ordem de prioridade:

* **Crítico:** Cadastro e verificação de usuários (clientes e profissionais), busca de serviços, agendamento e sistema de pagamento.  
* **Importante:** Sistema de avaliação, marketplace de produtos com integração logística.  
* **Útil:** Área de conteúdo informativo, planos premium para profissionais.

10. # **Requisitos de Documentação**

    1. ## **Manual do Usuário**

Será elaborado um manual de usuário online, com seções específicas para "Donos de Pet" e "Profissionais/Vendedores", explicando o funcionamento de todas as características da plataforma.

2. ## **Ajuda On-Line**

Uma seção de "Perguntas Frequentes" (FAQ) será implementada para auxiliar os usuários a resolverem dúvidas comuns de forma autônoma.

3. ## **Guias de Instalação, de Configuração e arquivo Leia-me**

Não se aplica para o usuário final, mas a documentação técnica de implantação do sistema será criada para a equipe de desenvolvimento.

11. # **Anexos**

Entrevista: https://github.com/ps-es-2025-2/geral/tree/main/atividade-09-03-1/projeto-marketplace-de-pets

