# Problemas Encontrados e Soluções

## Erro de AMI Inválida

### Problema

A AMI utilizada originalmente não existia na região selecionada.

### Solução

Utilização do AWS Systems Manager Parameter Store:

```yaml
Default: /aws/service/ami-amazon-linux-latest/al2023-ami-kernel-default-x86_64
```

---

## Dependência do Internet Gateway

### Problema

A rota para internet poderia ser criada antes do anexo do Internet Gateway.

### Solução

Adicionado:

```yaml
DependsOn: VPCGatewayAttachment
```

---

## Disponibilidade da Instância

### Problema

O tipo t2.micro pode não estar disponível em algumas regiões.

### Solução

Alterado para:

```yaml
InstanceType: t3.micro
```

---

## Chave SSH

### Problema

Falha ao criar a instância quando a Key Pair não existia.

### Solução

Criar previamente uma Key Pair e informar seu nome durante a criação da stack.

---

## Resultado Final

A stack foi criada com sucesso contendo:

* VPC
* Subnet Pública
* Internet Gateway
* Route Table
* Security Group
* Instância EC2
