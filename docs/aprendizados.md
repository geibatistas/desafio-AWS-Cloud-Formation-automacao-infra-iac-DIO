# Aprendizados Obtidos

## Infraestrutura como Código

Foi possível compreender como a infraestrutura pode ser descrita por código, permitindo:

* Reprodutibilidade
* Controle de versão
* Automação
* Padronização

## CloudFormation

Principais conceitos aprendidos:

### Resources

Representam os serviços AWS que serão criados.

Exemplos:

* AWS::EC2::VPC
* AWS::EC2::Subnet
* AWS::EC2::Instance

### Parameters

Permitem reutilizar o template em diferentes cenários.

### Outputs

Exibem informações importantes após a criação da stack.

### Dependências

O atributo DependsOn garante a ordem correta de criação dos recursos.

## Segurança

Foram aplicadas práticas básicas:

* Uso de Security Groups
* Separação de rede em VPC própria
* Controle de acesso por SSH

## GitHub

O GitHub foi utilizado para:

* Armazenamento do código
* Versionamento
* Compartilhamento da documentação
