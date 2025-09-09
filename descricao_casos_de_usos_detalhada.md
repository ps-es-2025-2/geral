# Descrição detalhada de cada Caso de Uso

## Grupo 1
| Aluno | Github |
|-------------|-------------|
|Gabriel Freitas dos Reis | GabrielFRails
|Gabriel Rodrigues Silva | Gabriellrs
|Laura Martins Vieira Gonçalves | lauramvg1821
|Léia Santos Costa | Leia27
|Tallya Jesus Sousa Barbosa | tallya01

---

## Nome
**Cadastrar Serviços e Preços**

## Descrição Sucinta
Permite à proprietária gerenciar os serviços oferecidos no salão, adicionando novos serviços, definindo seus preços e associando-os aos profissionais que os realizam.

## Atores
- **Proprietária (Administradora)**: Usuária responsável por gerenciar a lista de serviços.

## Pré-condição
A proprietária deve estar logada no sistema com privilégios de administrador.

## Pós-condições
- Um novo serviço é adicionado, atualizado ou removido do sistema.
- A lista de serviços e preços é atualizada para os clientes.
- A associação entre serviços e profissionais é atualizada.

## Fluxo Básico
1. A proprietária acessa o sistema de gerenciamento e seleciona a opção "**Gerenciar Serviços**".
2. O sistema exibe a lista atual de serviços cadastrados.
3. A proprietária pode optar por:
    - a) Adicionar um novo serviço.
    - b) Editar um serviço existente.
    - c) Remover um serviço existente.
4. **Para adicionar um novo serviço**:
    - A proprietária insere o **nome do serviço**, o **preço** e seleciona os **profissionais** que o realizam.
    - O sistema valida os dados e registra o novo serviço.
5. **Para editar um serviço**:
    - A proprietária seleciona um serviço da lista.
    - O sistema exibe os detalhes do serviço (nome, preço, profissionais).
    - A proprietária faz as alterações necessárias.
    - O sistema valida e atualiza as informações do serviço.
6. **Para remover um serviço**:
    - A proprietária seleciona um serviço da lista.
    - O sistema solicita uma **confirmação para a exclusão**.
    - A proprietária confirma.
    - O sistema remove o serviço da lista.
7. O sistema exibe uma mensagem de sucesso, confirmando a operação.
8. O caso de uso é concluído.

## Fluxos Alternativos
- **A1: Busca por serviço**: No passo 2, a proprietária pode usar um campo de busca para encontrar um serviço específico, facilitando a edição ou remoção em listas longas.

## Fluxos de Exceção
- **E1: Falha na validação de dados**: Nos passos 4 e 5, se a proprietária inserir dados inválidos (ex: preço negativo, nome do serviço em branco), o sistema exibe uma mensagem de erro e pede a correção.
- **E2: Serviço com agendamentos futuros**: No passo 6, se o serviço que a proprietária tentar remover tiver agendamentos futuros, o sistema impede a exclusão e exibe uma mensagem de aviso, sugerindo que o serviço seja desativado em vez de excluído.

## Estrutura de Dados
### Serviço
- ID do serviço (chave primária)
- Nome do serviço
- Preço
- Status (ativo/inativo)

### Profissional
- ID do profissional (chave primária)
- Nome do profissional

### Tabela de Relacionamento
- ID do serviço (chave estrangeira)
- ID do profissional (chave estrangeira)

## Regras de Negócio
- **RN1**: Apenas a proprietária pode cadastrar, editar ou remover serviços.
- **RN2**: Todos os campos obrigatórios (**nome**, **preço**) devem ser preenchidos.
- **RN3**: O **preço** deve ser um valor numérico positivo.
- **RN4**: Um serviço só pode ser excluído se não houver agendamentos futuros associados a ele.

## Observações
- Este caso de uso é fundamental para a gestão do negócio, garantindo que o aplicativo reflita a oferta de serviços real do salão.

### Descrição detalhada do Caso de Uso - Visualizar lista de serviços com preços

#### Nome
**Visualizar lista de serviços com preços**

#### Descrição Sucinta
Permite ao **cliente** ver uma lista de todos os serviços oferecidos pelo salão, juntamente com seus respectivos preços, para que ele possa escolher qual serviço deseja agendar.

#### Atores
- **Cliente**

#### Pré-condição
O cliente acessou o aplicativo.

#### Pós-condições
O cliente visualizou a lista de serviços e preços.

#### Fluxo Básico
1. O cliente abre o aplicativo "Beleza & Estilo".
2. O sistema exibe a página principal, que inclui a opção para visualizar serviços.
3. O cliente seleciona a opção para visualizar a lista de serviços.
4. O sistema busca no banco de dados a lista de serviços e seus preços.
5. O sistema exibe a lista de serviços, mostrando o nome de cada serviço e o preço associado.
6. O caso de uso é concluído.

#### Fluxos Alternativos
- **A1: Sem serviços cadastrados**: Se a proprietária ainda não cadastrou nenhum serviço, o sistema exibe uma mensagem informando que não há serviços disponíveis no momento.

#### Fluxos de Exceção
- **E1: Erro de conexão**: Se houver um problema de conexão com a internet ou com o servidor, o sistema exibe uma mensagem de erro, solicitando que o cliente tente novamente mais tarde.

#### Estrutura de Dados
- **Serviço**:
  - Nome do serviço
  - Preço
  - Descrição (opcional)

#### Regras de Negócio
- **RN1**: A lista de serviços e preços deve estar sempre atualizada com base nos dados cadastrados pela proprietária.
- **RN2**: A visualização dos serviços não requer login.

---

### Descrição detalhada do Caso de Uso - Consultar horários disponíveis

#### Nome
**Consultar horários disponíveis**

#### Descrição Sucinta
Permite ao **cliente** verificar os horários em que os profissionais estão livres para agendamentos, com base em um serviço específico.

#### Atores
- **Cliente**

#### Pré-condição
O cliente selecionou um serviço para agendar.

#### Pós-condições
O cliente visualizou os horários disponíveis para o serviço e profissional selecionados.

#### Fluxo Básico
1. O cliente, após selecionar um serviço, escolhe um profissional ou opta por ver a disponibilidade de todos os profissionais.
2. O sistema acessa a agenda de trabalho do(s) profissional(is) e os agendamentos já existentes.
3. O sistema compara a agenda de trabalho com os agendamentos confirmados para identificar os horários livres.
4. O sistema exibe os horários disponíveis em uma lista, organizados por dia e horário.
5. O cliente visualiza a lista e pode selecionar um horário.
6. O caso de uso é concluído.

#### Fluxos Alternativos
- **A1: Não há horários disponíveis**: Se o sistema não encontrar horários livres para o serviço e profissional selecionado, ele informa o cliente e sugere a busca por outro profissional ou outro dia.

#### Fluxos de Exceção
- **E1: Falha na comunicação**: Se houver um erro na comunicação com o servidor ao buscar os dados da agenda, o sistema exibe uma mensagem de erro e pede para o cliente tentar novamente.

#### Estrutura de Dados
- **Agendamento**:
  - Data e hora
  - ID do profissional
  - ID do cliente (se já agendado)

- **Profissional**:
  - ID do profissional
  - Horário de trabalho (por exemplo, 09:00 - 18:00)

#### Regras de Negócio
- **RN1**: Um horário é considerado disponível apenas se estiver dentro do horário de trabalho do profissional e não houver um agendamento confirmado.
- **RN2**: A consulta pode ser feita sem que o cliente tenha um cadastro prévio.

---

### Descrição detalhada do Caso de Uso - Cadastrar cliente

#### Nome
**Cadastrar cliente**

#### Descrição Sucinta
Permite ao **cliente** criar um cadastro simples no aplicativo, fornecendo informações essenciais como nome e telefone para agilizar futuros agendamentos e permitir o envio de notificações.

#### Atores
- **Cliente**

#### Pré-condição
O cliente acessou o aplicativo.

#### Pós-condições
- O cliente é registrado no sistema.
- Os dados do cliente são armazenados no banco de dados.

#### Fluxo Básico
1. O cliente acessa o aplicativo e seleciona a opção "Cadastrar-se".
2. O sistema exibe um formulário de cadastro.
3. O cliente insere seu **nome completo** e **telefone**.
4. O cliente confirma o cadastro.
5. O sistema valida os dados (por exemplo, formato do telefone) e verifica se o telefone já está cadastrado.
6. O sistema registra o novo cliente no banco de dados.
7. O sistema exibe uma mensagem de sucesso.
8. O caso de uso é concluído.

#### Fluxos Alternativos
- **A1: Cadastro durante o agendamento**: O cliente pode ser solicitado a se cadastrar no momento em que realiza um agendamento. O fluxo de cadastro é incorporado ao fluxo de agendamento.

#### Fluxos de Exceção
- **E1: Telefone já cadastrado**: Se o cliente tentar cadastrar um telefone que já existe no sistema, o sistema exibe uma mensagem informando que o cliente já possui um cadastro e sugere que ele continue o processo.
- **E2: Dados inválidos**: Se o cliente não preencher os campos obrigatórios ou inserir dados em um formato inválido, o sistema exibe uma mensagem de erro e pede a correção.

#### Estrutura de Dados
- **Cliente**:
  - ID do cliente (chave primária)
  - Nome
  - Telefone
  - Histórico de serviços (opcional)

#### Regras de Negócio
- **RN1**: O campo de telefone deve ser único e obrigatório.
- **RN2**: O nome também é um campo obrigatório.
- **RN3**: O sistema deve manter um cadastro simples, sem a necessidade de senha ou e-mail.

