## Enumerações do Sistema

O sistema utiliza enums para representar estados e perfis utilizados na aplicação.

---

### Perfil

Define os perfis de acesso do sistema.

| Código | Valor | Descrição |
|------|------|------|
| 0 | ADMIN | Administrador do sistema |
| 1 | CLIENTE | Usuário que abre chamados |
| 2 | TECNICO | Usuário responsável por atender chamados |

No banco de dados, os perfis são armazenados como **inteiros**.

---

### Status

Define o estado atual de um chamado.

| Código | Valor |
|------|------|
| 0 | ABERTO |
| 1 | ANDAMENTO |
| 2 | ENCERRADO |

---

### Prioridade

Define o nível de prioridade do chamado.

| Código | Valor |
|------|------|
| 0 | BAIXA |
| 1 | MEDIA |
| 2 | ALTA |