# Arquitetura da Solução

## Objetivo

Provisionar uma infraestrutura mínima na AWS utilizando AWS CloudFormation.

## Recursos Criados

### VPC

* CIDR: 10.0.0.0/16

### Subnet Pública

* CIDR: 10.0.1.0/24
* IP público habilitado

### Internet Gateway

Permite comunicação da VPC com a internet.

### Route Table

Responsável pelo roteamento do tráfego externo.

### Security Group

Portas liberadas:

| Porta | Protocolo | Finalidade |
| ----- | --------- | ---------- |
| 22    | TCP       | SSH        |
| 80    | TCP       | HTTP       |

### EC2

Características:

* Amazon Linux 2023
* Tipo t3.micro
* IP público automático

## Fluxo de Comunicação
```[text]
Internet
↓
Internet Gateway
↓
Route Table
↓
Subnet Pública
↓
EC2
```
