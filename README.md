# Sistema Bancário em Python

Bem-vindo ao **Sistema Bancário em Python**, um projeto desenvolvido para simular operações bancárias completas utilizando a linguagem de programação Python. Este sistema é ideal para quem está aprendendo programação e deseja compreender como implementar funcionalidades essenciais de um sistema financeiro, incluindo gestão de usuários e contas.

## Sumário

- [Descrição](#descrição)
- [Funcionalidades](#funcionalidades)
  - [Menu Principal](#menu-principal)
  - [Depósito](#depósito)
  - [Saque](#saque)
  - [Extrato](#extrato)
  - [Novo Usuário](#novo-usuário)
  - [Nova Conta](#nova-conta)
  - [Listar Contas](#listar-contas)
- [Como Usar](#como-usar)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Autor](#autor)
- [Licença](#licença)
- [Contato](#contato)
- [Agradecimentos](#agradecimentos)
- [Histórico de Versões](#histórico-de-versões)

## Descrição

O **Sistema Bancário em Python** é uma aplicação de console que permite aos usuários realizar operações bancárias completas, incluindo:

- **Gestão de Usuários**: Criação e gerenciamento de perfis de usuários.
- **Gestão de Contas**: Criação e listagem de contas bancárias associadas aos usuários.
- **Operações Financeiras**: Depósitos, saques e visualização de extratos.

O sistema é estruturado em várias funções, proporcionando uma experiência organizada e intuitiva para o usuário.

## Funcionalidades

### Menu Principal

O **Menu Principal** é a interface principal do sistema, onde o usuário pode selecionar a operação desejada. As opções disponíveis são:

- **[d] Depositar**: Permite ao usuário adicionar fundos à sua conta.
- **[s] Sacar**: Permite ao usuário retirar fundos da sua conta, com restrições aplicáveis.
- **[e] Extrato**: Exibe o histórico de transações realizadas na conta.
- **[nc] Nova Conta**: Permite a criação de uma nova conta bancária associada a um usuário existente.
- **[lc] Listar Contas**: Lista todas as contas bancárias existentes no sistema.
- **[nu] Novo Usuário**: Permite a criação de um novo perfil de usuário.
- **[q] Sair**: Encerra o sistema.

### Depósito

A funcionalidade de **Depósito** permite que o usuário adicione um valor positivo ao saldo da conta. O sistema valida se o valor informado é positivo antes de realizar a operação. Caso o valor seja inválido (não positivo), a operação é cancelada e uma mensagem de erro é exibida.

### Saque

A funcionalidade de **Saque** permite que o usuário retire fundos da sua conta, obedecendo às seguintes restrições:

- **Saldo Insuficiente**: O valor do saque não pode exceder o saldo disponível.
- **Limite de Saque**: Há um limite máximo por saque (R$ 500,00).
- **Número de Saques**: O usuário pode realizar no máximo 3 saques por dia.

Se alguma dessas condições não for atendida, o sistema informa o motivo da falha na operação.

### Extrato

A funcionalidade de **Extrato** exibe o histórico de todas as transações realizadas pelo usuário, incluindo depósitos e saques. Além disso, mostra o saldo atual da conta. Se nenhuma movimentação tiver sido realizada, o sistema informa que não há movimentações para exibir.

### Novo Usuário

A funcionalidade de **Novo Usuário** permite a criação de um novo perfil de usuário no sistema. O usuário deve fornecer:

- **CPF**: Cadastro de Pessoa Física (somente números).
- **Nome Completo**: Nome completo do usuário.
- **Data de Nascimento**: Formato `dd-mm-aaaa`.
- **Endereço**: Endereço completo (logradouro, número, bairro, cidade/estado).

O sistema verifica se já existe um usuário com o CPF informado. Caso exista, a criação do usuário é cancelada.

### Nova Conta

A funcionalidade de **Nova Conta** permite a criação de uma nova conta bancária associada a um usuário existente. O usuário deve fornecer o CPF do titular da conta. Se o usuário existir, a conta é criada com sucesso; caso contrário, a operação é cancelada.

### Listar Contas

A funcionalidade de **Listar Contas** exibe uma lista de todas as contas bancárias existentes no sistema, mostrando detalhes como:

- **Agência**: Número da agência bancária.
- **C/C**: Número da conta corrente.
- **Titular**: Nome do usuário associado à conta.
