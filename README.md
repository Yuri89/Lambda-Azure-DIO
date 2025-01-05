# httpValidCPF

Este repositório contém uma função Lambda do Azure que valida CPFs. A função aceita uma requisição HTTP (GET ou POST) contendo um CPF, e retorna se o CPF é válido ou não.

## Funcionalidade

A função verifica o formato e a validade do CPF informado, utilizando a formatação `xxx.xxx.xxx-xx` (apenas números, com pontos e hífen). Caso o CPF não seja válido, a função retorna um erro 400 com a mensagem correspondente. Caso o CPF seja válido, retorna uma resposta 200 com a confirmação de que o CPF é válido.

## Estrutura do Projeto

O projeto é uma **Função Azure** que usa o **C#** com a biblioteca **Azure Functions SDK**. O código realiza a validação do CPF utilizando uma expressão regular para garantir que o CPF tenha o formato correto e que os dígitos verificadores sejam válidos.

### Arquivos principais:

- `fnvalidacpf.cs`: Contém a lógica para validação do CPF.
- `function.json`: Configuração de binding da função HTTP.
