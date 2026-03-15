# Arquitetura da Aplicação

O projeto segue o padrão de arquitetura em camadas.

## Camadas da aplicação

### Controller

Responsável por expor os endpoints da API REST.

### Service

Contém as regras de negócio da aplicação.

### Repository

Responsável pelo acesso ao banco de dados utilizando Spring Data JPA.

### Domain

Contém as entidades do sistema.

```
domain
 ├ Pessoa
 ├ Cliente
 ├ Tecnico
 └ Chamado
```

### Enums

Representam estados e perfis utilizados no sistema.

```
Perfil
Status
Prioridade
```