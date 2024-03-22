# Point - Lambda Pré Sign-Up

## Introdução

Este projeto consiste em uma função Lambda na AWS que é acionada antes da confirmação do registro de um usuário no AWS Cognito. A função é responsável por configurar automaticamente a confirmação do usuário, permitindo o registro sem a necessidade de confirmação por e-mail ou SMS.

## Arquitetura

A arquitetura do projeto envolve os seguintes componentes:

1. Função Lambda: Implementa a lógica para configurar a confirmação automática do usuário.
2. AWS Cognito: Serviço de autenticação e autorização para aplicativos da web e dispositivos móveis.
3. Terraform: Utilizado para configurar e implantar recursos na AWS de forma automatizada e controlada.

## Fluxo de Trabalho

1. Um usuário tenta se registrar em um aplicativo que utiliza o AWS Cognito.
2. Antes da confirmação do registro, o AWS Cognito aciona a função Lambda configurada para o evento PreSignUp.
3. A função Lambda recebe o evento, configura a propriedade autoConfirmUser como True e retorna o evento modificado.
4. Com a propriedade configurada, o AWS Cognito confirma automaticamente o registro do usuário.

## Configuração

Antes de implantar a função Lambda, é necessário configurar os seguintes recursos:

1. AWS Cognito User Pool: Um pool de usuários do AWS Cognito onde os usuários serão registrados.
2. AWS IAM Role: Uma função IAM que permite que a função Lambda assuma o controle dos recursos necessários.
3. Lambda Function: A função Lambda que contém a lógica para configurar a confirmação automática do usuário.

## Implantação

A implantação do projeto é realizada da seguinte maneira:

1. Os arquivos de configuração Terraform são preparados com as informações necessárias, como região da AWS e IDs de usuário do AWS Cognito.
2. Os recursos são criados e implantados na AWS usando o Terraform.
3. A função Lambda é configurada para ser acionada antes da confirmação do registro de um usuário no AWS Cognito.

## Recursos

- Terraform: Utilizado para a automação da infraestrutura na AWS.
- AWS Lambda: Serviço de computação serverless da AWS.
- AWS Cognito: Serviço de autenticação e autorização da AWS.
- Python 3.11: Linguagem de programação utilizada para a implementação da lógica da função Lambda.

## Conclusão

Este projeto oferece uma solução simples e eficaz para configurar a confirmação automática de usuários no AWS Cognito, eliminando a necessidade de confirmação por e-mail ou SMS. Ele pode ser facilmente integrado a aplicativos que utilizam o AWS Cognito para autenticação, proporcionando uma experiência de registro mais rápida e conveniente para os usuários.
