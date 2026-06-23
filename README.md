# Desafio-AWS-Cloud-Formation-automacao-infra-iac-DIO

## Descrição

Este projeto foi desenvolvido como parte do desafio prático de Infraestrutura como Código (IaC) utilizando AWS CloudFormation.

O objetivo foi automatizar a criação de recursos na AWS por meio de um template YAML, aplicando conceitos de padronização, replicação, automação e segurança.

A solução provisiona automaticamente:

* VPC personalizada
* Subnet pública
* Internet Gateway
* Tabela de rotas
* Security Group
* Instância EC2 Amazon Linux

---

## Arquitetura Implementada
```
A infraestrutura criada possui os seguintes componentes:

VPC (10.0.0.0/16)
│
├── Subnet Pública (10.0.1.0/24)
│
├── Internet Gateway
│
├── Route Table
│
└── EC2 (Amazon Linux 2023)
```
---

## Tecnologias Utilizadas

* AWS CloudFormation
* Amazon EC2
* Amazon VPC
* AWS Systems Manager Parameter Store (SSM)
* Git
* GitHub

---

## Estrutura do Projeto

```text
cloudformation/
└── infraestrutura-basica.yaml

docs/
├── arquitetura.md
├── aprendizados.md
└── troubleshooting.md

images/
```

## Como Executar

### 1. Criar uma Key Pair

No console EC2:

* Acesse Key Pairs
* Clique em Create Key Pair
* Informe um nome
* Faça download do arquivo .pem

### 2. Criar a Stack

Acesse:

CloudFormation → Create Stack → With new resources

Selecione o arquivo:

```text
infraestrutura-basica.yaml
```

Informe o parâmetro:

```text
KeyName
```

Utilizando o nome da Key Pair criada.

### 3. Provisionamento

Após alguns minutos a stack será criada e os recursos ficarão disponíveis para uso.

---

## Evidências

Adicionar capturas de tela na pasta images:

* Stack criada com sucesso
* Recursos provisionados
* Instância EC2 em execução
* Outputs do CloudFormation

---

## Aprendizados

Durante o desenvolvimento foram praticados:

* Criação automatizada de infraestrutura
* Utilização de templates YAML
* Gerenciamento de dependências entre recursos
* Uso de parâmetros dinâmicos
* Boas práticas de segurança em redes AWS
* Versionamento de infraestrutura com GitHub

---

## Autor

Projeto desenvolvido para fins educacionais como parte do laboratório de AWS CloudFormation.

