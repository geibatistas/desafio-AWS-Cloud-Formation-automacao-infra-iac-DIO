# Desafio AWS CloudFormation - Automação de Infraestrutura com IaC

![AWS](https://img.shields.io/badge/AWS-CloudFormation-orange?logo=amazonaws)
![IaC](https://img.shields.io/badge/Infrastructure%20as%20Code-IaC-blue)
![YAML](https://img.shields.io/badge/YAML-Template-red)
![GitHub](https://img.shields.io/badge/GitHub-Documentation-black?logo=github)

## 📖 Sobre o Projeto

Este projeto foi desenvolvido como parte do desafio prático da DIO com foco em **Infraestrutura como Código (IaC)** utilizando **AWS CloudFormation**.

O objetivo é demonstrar como automatizar o provisionamento de recursos na AWS através de um template YAML, aplicando conceitos fundamentais de:

* Padronização de infraestrutura
* Automação de provisionamento
* Reutilização de código
* Segurança básica em ambientes cloud
* Versionamento utilizando Git e GitHub

---

## 🎯 Objetivos de Aprendizagem

Durante a execução deste laboratório foram praticados os seguintes conceitos:

✅ Criação de infraestrutura utilizando CloudFormation

✅ Utilização de templates YAML

✅ Provisionamento automatizado de recursos AWS

✅ Documentação técnica em GitHub

✅ Aplicação de boas práticas de Infraestrutura como Código

---

## 🏗️ Arquitetura Implementada

A solução provisiona automaticamente os seguintes recursos:

* VPC personalizada
* Subnet Pública
* Internet Gateway
* Route Table
* Security Group
* Instância EC2 Amazon Linux 2023

### Diagrama Lógico

```text
Internet
    │
    ▼
Internet Gateway
    │
    ▼
Route Table
    │
    ▼
Subnet Pública (10.0.1.0/24)
    │
    ▼
EC2 Amazon Linux 2023
    │
    ▼
VPC (10.0.0.0/16)
```

---

## ⚙️ Tecnologias Utilizadas

| Tecnologia              | Finalidade                        |
| ----------------------- | --------------------------------- |
| AWS CloudFormation      | Provisionamento da infraestrutura |
| Amazon EC2              | Máquina virtual                   |
| Amazon VPC              | Rede privada virtual              |
| AWS SSM Parameter Store | Obtenção dinâmica da AMI          |
| YAML                    | Definição do template             |
| Git                     | Controle de versão                |
| GitHub                  | Compartilhamento do projeto       |

---

## 📂 Estrutura do Projeto

```text
📦 aws-cloudformation-lab
│
├── cloudformation
│   └── infraestrutura-basica.yaml
│
├── docs
│   ├── arquitetura.md
│   ├── aprendizados.md
│   └── troubleshooting.md
│
├── images
│   ├── stack-created.png
│   ├── resources.png
│   └── ec2-running.png
│
└── README.md
```

---

## 🚀 Como Executar

### 1️⃣ Criar uma Key Pair

No console AWS:

EC2 → Key Pairs → Create Key Pair

Salve o arquivo `.pem` gerado.

---

### 2️⃣ Criar a Stack

Acesse:

```text
CloudFormation → Create Stack → With new resources
```

Selecione o template:

```text
infraestrutura-basica.yaml
```

Informe o parâmetro:

```text
KeyName
```

Utilizando o nome da Key Pair criada anteriormente.

---

### 3️⃣ Provisionar os Recursos

Após alguns minutos a stack será criada automaticamente e todos os recursos estarão disponíveis na conta AWS.

---

## 📸 Evidências

Adicionar capturas de tela na pasta `/images`:

* Stack criada com sucesso
* Recursos provisionados
* Instância EC2 em execução
* Outputs do CloudFormation

Exemplo:

```text
images/
├── stack-created.png
├── resources.png
└── ec2-running.png
```

---

## 📚 Principais Aprendizados

Durante a realização deste desafio foi possível compreender:

* Como descrever infraestrutura através de código
* Como reutilizar ambientes utilizando templates
* A importância do controle de versão para infraestrutura
* Como gerenciar dependências entre recursos AWS
* Como utilizar parâmetros dinâmicos para evitar configurações fixas
* Boas práticas básicas de segurança em ambientes cloud

---

## ✅ Resultado

Ao final do laboratório foi possível criar uma infraestrutura completa de forma automatizada utilizando apenas um template CloudFormation, demonstrando os benefícios da abordagem Infrastructure as Code (IaC).

---

## 👨‍💻 Autor

Projeto desenvolvido para fins educacionais como parte do desafio da DIO sobre AWS CloudFormation e Infraestrutura como Código.
