# Modelo de Banco de Dados

O banco de dados segue o modelo relacional baseado nas entidades do domínio.

## Tabelas principais

- pessoa
- cliente
- tecnico
- chamado

## Relacionamentos

Cliente → 1:N → Chamado

Tecnico → 1:N → Chamado

## Campos principais

### Pessoa

- id
- nome
- cpf
- email
- senha
- dataCriacao

### Chamado

- id
- dataAbertura
- dataFechamento
- prioridade
- status
- titulo
- observacoes