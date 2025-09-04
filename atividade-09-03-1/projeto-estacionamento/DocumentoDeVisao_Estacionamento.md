# Documento de Visão

Documento de visão para o projeto Estacionamento PS-2025 Atividade 09-03-1

Produzido por Felipe Alves Leão de Araújo (Analista de Requisitos)

## Introdução

O software define um aplicativo que vai ser usado por funcionários e gerência de um estacionamento e contém funções de manejo desse estacionamento: registro de movimento de veículos, cálculo do valor, controle de vagas, registro da placa e relatórios. Essas funções todas são partes do MVP.

## Análise de Contexto

### Descrição do Problema
Esse estacionamento não usa nenhum sistema atualmente, o controle é feito manualmente (papel e caneta). A função do sistema é diminuir o número de erros, atraso e criar registros.
### Partes Afetadas
O cliente é uma parte afetada quando o assunto é atraso, mas o estabalecimento também sofre com perca de eficiência.
### Impacto
O problema pode causar insatisfação do cliente, que pode ir atrás de outro estacionamento.
Para o estabelecimento, isso é um impacto financeiro.
### Solução de Sucesso
A solução de sucesso necessariamente precisa ser mais eficiente que o sistema de papel e caneta. Essa eficiência vem em forma de velocidade (menos atrasos) e uma menor margem de erro para o atendente - registro de dados deve ser fácil e eficiente. 

## Partes Interessadas
### Partes Interessadas
|Unidade|Representada Por  | Envolvimento Com O Projeto|
|--|--|-- |
|Estacionamento  | Carlos (Gerente) | Contato com a equipe e define os problemas |
|Equipe de Software| Felipe (Analista de Requisitos) | Criou os requisitos a partir dos problemas ; Contato com o cliente

### Usuários
1.
<table>
  <tr>
    <th>Tipo de Usuário</th>
    <td>Funcionário</td>
  </tr>
  <tr>
    <th>Representante</th>
    <td>Funcionário A </td>
  </tr>
    <tr>
    <th>Descrição</th>
    <td>Funcionário do estacionamento, que faz o controle e registro dos veículos. Usuário principal do aplicativo.</td>
  </tr>
  <tr>
    <th>Responsabilidades</th>
    <td>Registro de check-in e check-out, registro de placas</td>
  </tr>
</table> 
	  2.
<table>
  <tr>
    <th>Tipo de Usuário</th>
    <td>Gerente</td>
  </tr>
  <tr>
    <th>Representante</th>
    <td>Carlos </td>
  </tr>
    <tr>
    <th>Descrição</th>
    <td>Gerente do estacionamento, usa os dados do aplicativo.</td>
  </tr>
  <tr>
    <th>Responsabilidades</th>
    <td>Uso dos relatórios gerados pelo aplicativo para a inteligência do negócio</td>
  </tr>
</table>

## Objetivos do Negócio

|Objetivo do Negócio|Descrição  |
|--|--|
|Agilidade  |Agilidade das operações para maior satisfação com o cliente  |
|Eficácia |A quantidade de erros cometidos deve ser menor  |
|Relevância de dados |Os dados coletados e relatórios gerados devem condizer com necessidades de negócio |


## Visão Geral do Produto

### Perspectiva do Produto
O produto é um sistema isolado que só existe no contexto desse estacionamento. Não há nenhum tipo de integração. Esse produto é um aplicativo de desktop que existe localmente e não depende de acesso de rede
### Características chaves do produto
| Característica-chave | Descrição | Prioridade |
|--|--| -- |
| Check-in e check-out de veículos. | Registra quais veículos estão entrando e saíndo do estacionamento  | 1|
| Cálculo de Preço | Cálculo automático do valor com base no tempo  | 1|
| Controle de Vagas |  Controle de vagas disponíveis e ocupadas.  | 2|
| Registro da placa do veículo |  Registro manual da placa do veículo entrando no estacionamento| 3|
| Relatórios básicos |  faturamento, tempo médio, ocupação, horário de pico  | 4|
| Registro avançado da placa do veículo |  Uso de OCR para registro da placa de veículo|5|


###  Requisitos Não Funcionais

|Tipo|Descrição  | Prioridade|
|--|--|--|
|Usabilidade  | Maior prioridade - caso manusear o sistema seja mais lento que papel e caneta, o produto não soluciona o problema encontrado |1 |
|Acessibilidade | Sistmea vai ser usado por poucas pessoas. O caso para a acessibilidade é menos importante.| 3|
|Confiabilidade | Realisticamente, o estacionamento não para de funcionar se o sistema não funcionar - o sistema de papel e caneta existe como backup. O problema de confiabilidade é majoritariamente resolvido pelo sistema não precisar de conexão com internet.| 2|
|Desempenho| Grande prioridade pelo mesmo motivo que usabilidade - deve ser melhor que a operação manual do estacionamento| 1|
|Segurança| Por segurança de negócio, precisa de autenticação e soluções de segurança mas não é prioridade máxima por ser um sistema local com pouca superfícies de ataque |2 |
|Interface| Interface eficiente com o mínimo de passos possíveis é importante para a eficiência do negócio. Problemas menores de interface não vão impedir o funcionamento. | 2|

