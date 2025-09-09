# Atividade 09-03-1 — Casos de Uso Detalhados

---

## Módulo de Gestão de Contas

Este módulo agrupa as funcionalidades essenciais para o gerenciamento de contas de todos os usuários da plataforma.

### UC01: Realizar Cadastro

**Nome:** Realizar Cadastro

**Descrição sucinta:** Permite que um novo usuário (Dono de Pet ou Profissional/Vendedor) crie uma conta de acesso à plataforma.

**Atores:** Usuário (Dono de Pet, Profissional/Vendedor).

**Pré-condições:**

- O usuário não deve possuir um cadastro ativo com o e-mail informado.

**Pós-condições:**

- Uma nova conta de usuário é criada no sistema.
- Se o usuário for do tipo "Profissional/Vendedor", seu perfil é marcado como "Pendente de Validação".
- O usuário é autenticado e redirecionado para a página principal.

**Fluxo Básico:**

1. O usuário seleciona a opção "Cadastrar-se".
2. O sistema solicita que o usuário escolha o tipo de perfil ("Dono de Pet" ou "Profissional/Vendedor").
3. O usuário preenche o formulário com seus dados (nome, e-mail, senha).
4. O usuário confirma a submissão do formulário.
5. O sistema valida os dados e verifica a regra de negócio (RN1).
6. O sistema cria a conta do usuário.
7. O sistema realiza o login automático do usuário.
8. O caso de uso é encerrado.

**Fluxo Alternativo:**

- (A1) **E-mail já cadastrado (Passo 5):**
  - O sistema exibe a mensagem "O e-mail informado já está em uso".
  - O sistema retorna ao Passo 3.

**Regra de Negócio:**

- (RN1) O e-mail do usuário deve ser único na plataforma.

---

### UC02: Realizar Login

**Nome:** Realizar Login

**Descrição sucinta:** Autentica um usuário já cadastrado para que ele possa acessar as funcionalidades restritas da plataforma.

**Atores:** Usuário (Dono de Pet, Profissional/Vendedor, Administrador).

**Pré-condições:**

- O usuário deve possuir uma conta ativa no sistema.

**Pós-condições:**

- O usuário é autenticado no sistema.
- O usuário tem acesso às funcionalidades correspondentes ao seu perfil.

**Fluxo Básico:**

1. O usuário seleciona a opção "Login".
2. O usuário informa seu e-mail e senha.
3. O usuário seleciona a opção "Entrar".
4. O sistema valida as credenciais.
5. O sistema concede acesso à plataforma.
6. O caso de uso é encerrado.

**Fluxo Alternativo:**

- (A1) **Credenciais inválidas (Passo 4):**
  - O sistema exibe a mensagem "E-mail ou senha inválidos".
  - O sistema retorna ao Passo 2.

---

## Módulo de Marketplace

Este módulo contém as funcionalidades centrais da plataforma, permitindo a busca, contratação e compra de serviços e produtos.

### UC03: Buscar Serviços/Produtos

**Nome:** Buscar Serviços/Produtos

**Descrição sucinta:** Permite que qualquer usuário (logado ou não) pesquise por serviços e produtos disponíveis na plataforma utilizando filtros.

**Atores:** Usuário (Dono de Pet, Profissional/Vendedor), Visitante (não logado).

**Pré-condições:** Nenhuma.

**Pós-condições:**

- A lista de resultados correspondente à busca é exibida para o usuário.

**Fluxo Básico:**

1. O usuário acessa a página de busca.
2. O usuário insere termos de busca e/ou aplica filtros.
3. O usuário aciona a busca.
4. O sistema consulta a base de dados e retorna os perfis de profissionais e lojas que atendem aos critérios.
5. O sistema exibe a lista de resultados.
6. O caso de uso é encerrado.

**Fluxo Alternativo:**

- (A1) **Nenhum resultado encontrado (Passo 4):**
  - O sistema exibe a mensagem "Nenhum resultado encontrado para sua busca".
  - O caso de uso é encerrado.

---

### UC04: Agendar Serviço

**Nome:** Agendar Serviço

**Descrição sucinta:** Permite que um Dono de Pet contrate e agende um serviço com um profissional.

**Atores:** Dono de Pet.

**Pré-condições:**

- O Dono de Pet deve ter executado o caso de uso "Realizar Login".

**Pós-condições:**

- O agendamento é registrado no sistema.
- A agenda do profissional é atualizada.
- O pagamento é processado.

**Fluxo Básico:**

1. O Dono de Pet seleciona um serviço no perfil de um profissional.
2. O sistema exibe a agenda do profissional com os horários disponíveis.
3. O Dono de Pet seleciona a data e o horário desejado.
4. O Dono de Pet confirma a seleção.
5. O sistema executa o caso de uso **UC07: Realizar Pagamento**.
6. Após a confirmação do pagamento, o sistema registra o agendamento.
7. O sistema notifica o Dono de Pet e o Profissional sobre o novo agendamento.
8. O caso de uso é encerrado.

**Fluxo Alternativo:**

- (A1) **Falha no pagamento (Passo 5):**
  - O sistema exibe uma mensagem de erro no pagamento.
  - O sistema cancela a pré-reserva do horário.
  - O caso de uso é encerrado.

---

## Módulo do Profissional

Este módulo contém as ferramentas para que profissionais e vendedores gerenciem sua presença e operações na plataforma.

### UC05: Gerenciar Perfil Profissional

**Nome:** Gerenciar Perfil Profissional

**Descrição sucinta:** Permite que o profissional/vendedor edite as informações de seu perfil público, adicione documentos para validação e configure seus serviços.

**Atores:** Profissional/Vendedor.

**Pré-condições:**

- O Profissional/Vendedor deve ter executado o caso de uso "Realizar Login".

**Pós-condições:**

- As informações do perfil do profissional são atualizadas no sistema.

**Fluxo Básico:**

1. O profissional acessa a área "Meu Perfil".
2. O profissional edita suas informações (descrição, fotos, contatos, documentos).
3. O profissional salva as alterações.
4. O sistema atualiza os dados no banco de dados.
5. O sistema exibe a mensagem "Perfil atualizado com sucesso".
6. O caso de uso é encerrado.

---

### UC06: Gerenciar Agenda/Pedidos

**Nome:** Gerenciar Agenda/Pedidos

**Descrição sucinta:** Permite que o profissional/vendedor visualize e administre os agendamentos de serviços e pedidos de produtos recebidos.

**Atores:** Profissional/Vendedor.

**Pré-condições:**

- O Profissional/Vendedor deve ter executado o caso de uso "Realizar Login".

**Pós-condições:**

- O status de um agendamento ou pedido é atualizado (ex: confirmado, cancelado, concluído).

**Fluxo Básico:**

1. O profissional acessa seu painel de controle em "Agenda" ou "Pedidos".
2. O sistema exibe a lista de agendamentos/pedidos com seus respectivos status.
3. O profissional seleciona um item da lista.
4. O profissional realiza uma ação (confirmar, marcar como concluído, cancelar).
5. O sistema atualiza o status do agendamento/pedido.
6. O sistema notifica o Dono de Pet sobre a alteração.
7. O caso de uso é encerrado.

---

## Módulo de Avaliação e Conteúdo

Este módulo visa aumentar a confiança e o engajamento na plataforma.

### UC07: Avaliar Serviço/Produto

**Nome:** Avaliar Serviço/Produto

**Descrição sucinta:** Permite que um Dono de Pet avalie um serviço ou produto após sua conclusão/recebimento.

**Atores:** Dono de Pet.

**Pré-condições:**

- O Dono de Pet deve ter executado o caso de uso "Realizar Login".
- O serviço deve estar com status "Concluído" ou o produto com status "Entregue".

**Pós-condições:**

- A avaliação é registrada e associada ao perfil do profissional/vendedor.
- A nota média do profissional/vendedor é recalculada.

**Fluxo Básico:**

1. O Dono de Pet acessa "Meus Pedidos".
2. Seleciona um serviço/produto concluído que ainda não foi avaliado.
3. Seleciona a opção "Avaliar".
4. O sistema exibe o formulário de avaliação.
5. O Dono de Pet preenche a avaliação (nota em estrelas e comentário).
6. O Dono de Pet envia a avaliação.
7. O sistema salva a avaliação.
8. O caso de uso é encerrado.

---

## Módulo de Administração

Este módulo agrupa funcionalidades restritas aos administradores da plataforma PETCONNECT.

### UC08: Validar Perfil de Profissional

**Nome:** Validar Perfil de Profissional

**Descrição sucinta:** Permite que o Administrador revise e aprove ou reprove o cadastro de um novo profissional/vendedor, garantindo a transparência e segurança. Este caso de uso estende o "Realizar Cadastro".

**Atores:** Administrador.

**Pré-condições:**

- O Administrador deve ter executado o caso de uso "Realizar Login".
- Deve existir pelo menos um perfil de profissional com o status "Pendente de Validação".

**Pós-condições:**

- O perfil do profissional é atualizado para "Validado" ou "Reprovado".

**Fluxo Básico:**

1. O Administrador acessa "Validações Pendentes".
2. O sistema exibe a lista de profissionais aguardando validação.
3. O Administrador seleciona um perfil.
4. O sistema exibe os dados e documentos enviados.
5. O Administrador analisa as informações.
6. O Administrador seleciona "Aprovar" ou "Reprovar".
7. O sistema atualiza o status.
8. O sistema notifica o profissional.
9. O caso de uso é encerrado.

**Fluxo Alternativo:**

- (A1) **Informações insuficientes (Passo 6):**
  - O Administrador seleciona "Solicitar mais informações".
  - O sistema altera o status do perfil para "Informações Pendentes".
  - O sistema envia uma notificação ao profissional detalhando as informações necessárias.
  - O caso de uso é encerrado.
