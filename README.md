# Infraestrutura-Automatizada-AWS-CloudFormation
Este repositório serve como material de apoio para estudos e futuras implementações sobre infraestrutura automatizada com AWS CloudFormation


# Conceito

Infraestrutura automatizada significa criar, gerenciar e atualizar recursos de nuvem de forma programática, sem precisar configurar cada recurso manualmente.
O AWS CloudFormation é a ferramenta da AWS que permite fazer isso usando templates declarativos (YAML ou JSON).

Em vez de clicar no console várias vezes, você escreve o “plano da infraestrutura” e a AWS executa tudo automaticamente.

# Benefícios da automação

Velocidade e eficiência

Ambientes inteiros podem ser provisionados em minutos, independentemente do número de recursos.

Consistência

Todos os ambientes criados a partir do mesmo template são idênticos, eliminando erros humanos.

Reprodutibilidade

Você pode criar múltiplos ambientes de teste, desenvolvimento e produção com a mesma infraestrutura.

Controle de versão

Templates podem ser versionados no Git, permitindo auditoria e histórico de alterações.

Rollback automático

Se a criação ou atualização falhar, o CloudFormation desfaz automaticamente as mudanças para evitar inconsistências.

Documentação viva

O template funciona como documentação atualizada da sua infraestrutura.

# Como funciona na prática

Escrever um template

Define recursos, parâmetros, outputs e dependências.

Criar uma stack

O template é enviado para o CloudFormation, que provisiona todos os recursos de acordo com a descrição.

Atualizar ou deletar stacks

Alterações na infraestrutura podem ser feitas alterando o template e aplicando a atualização.

Ao deletar a stack, todos os recursos são removidos automaticamente.

# Componentes principais de um template

Resources: recursos AWS a serem criados (EC2, S3, Lambda, VPC, RDS etc.)

Parameters: valores configuráveis pelo usuário no deploy

Outputs: informações úteis para referência posterior

Mappings: tabelas estáticas para definir configurações específicas

Conditions: regras condicionais para criação de recursos

Transform: permite incluir stacks externas ou macros

# Boas práticas

Modularizar templates com nested stacks

Utilizar parâmetros e variáveis para tornar templates reutilizáveis

Versionar templates no Git

Testar templates com validate-template

Aplicar tags para gestão e rastreamento de recursos

# Resumo:
Infraestrutura automatizada com CloudFormation é Infrastructure as Code (IaC) aplicada na prática. Você descreve sua infraestrutura como código, a AWS provisiona tudo automaticamente, garantindo consistência, eficiência e escalabilidade.