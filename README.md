# 🛠 Helpdesk API

![Java](https://img.shields.io/badge/Java-11-red)
![Spring Boot](https://img.shields.io/badge/SpringBoot-2.3-green)
![Maven](https://img.shields.io/badge/Maven-Build-blue)
![MySQL](https://img.shields.io/badge/MySQL-Database-orange)
![License](https://img.shields.io/badge/license-MIT-green)

API REST desenvolvida com **Spring Boot** para gerenciamento de chamados de suporte técnico.

O sistema permite o cadastro de **clientes, técnicos e chamados**, possibilitando o acompanhamento do ciclo de atendimento de suporte.

---

## 🚀 Tecnologias

- Java
- Spring Boot
- Spring Data JPA
- Spring Security
- Maven
- MySQL
- H2 Database

---

## 🏗 Arquitetura da aplicação

A aplicação segue o padrão de arquitetura em camadas.

```text
Cliente / Postman
       ↓
Controller
       ↓
Service
       ↓
Repository
       ↓
Database
```

### Camadas da aplicação

- **Controller** → expõe os endpoints da API
- **Service** → contém as regras de negócio
- **Repository** → responsável pelo acesso ao banco de dados
- **Database** → persistência das informações

---

## 🧠 Modelo de Domínio

O sistema Helpdesk foi modelado utilizando orientação a objetos.

A entidade **Pessoa** representa os usuários do sistema e possui duas especializações:

- Cliente
- Técnico

A entidade **Chamado** representa os tickets de atendimento.

Além das entidades principais, o sistema utiliza enums para representar regras de negócio:

- **Perfil** → define os perfis de acesso do usuário
- **Status** → define a situação do chamado
- **Prioridade** → define o nível de prioridade do chamado

### Relacionamentos

- Um **Cliente** pode possuir vários **Chamados**
- Um **Técnico** pode atender vários **Chamados**
- Cada **Chamado** pertence a um cliente e é atendido por um técnico

### Enums do sistema

**Perfil**
- ADMIN
- CLIENTE
- TECNICO

**Status**
- ABERTO
- ANDAMENTO
- ENCERRADO

**Prioridade**
- BAIXA
- MEDIA
- ALTA

### Diagrama do Modelo Conceitual

![Modelo Conceitual](docs/modelo-conceitual.png)

---

## 📡 Endpoints da API

| Método | Endpoint | Descrição |
|------|------|------|
| GET | `/clientes` | Lista todos os clientes |
| GET | `/clientes/{id}` | Busca cliente por ID |
| POST | `/clientes` | Cria um novo cliente |
| PUT | `/clientes/{id}` | Atualiza um cliente |
| DELETE | `/clientes/{id}` | Remove um cliente |
| GET | `/tecnicos` | Lista todos os técnicos |
| GET | `/tecnicos/{id}` | Busca técnico por ID |
| POST | `/tecnicos` | Cria um novo técnico |
| PUT | `/tecnicos/{id}` | Atualiza um técnico |
| DELETE | `/tecnicos/{id}` | Remove um técnico |
| GET | `/chamados` | Lista todos os chamados |
| GET | `/chamados/{id}` | Busca chamado por ID |
| POST | `/chamados` | Cria um chamado |
| PUT | `/chamados/{id}` | Atualiza um chamado |
| DELETE | `/chamados/{id}` | Remove um chamado |

---

## 📂 Estrutura do Projeto

```text
src
 └─ main
    └─ java
       └─ com.nobre.helpdesk
          ├─ controller
          ├─ service
          ├─ repository
          ├─ domain
          └─ domain.enums
```

---

## ▶️ Como executar o projeto

### Pelo Spring Tool Suite (STS)

1. Abra a classe principal:

```text
HelpdeskApplication.java
```

2. Clique com o botão direito

```text
Run As → Spring Boot App
```

A aplicação iniciará em:

```text
http://localhost:8080
```

![Executando Spring Boot](docs/run-spring-boot.png)

---

### Pelo terminal

Dentro da pasta do projeto execute:

```bash
mvn spring-boot:run
```

---

## 🧪 Banco H2

Console disponível em:

```text
http://localhost:8080/h2-console
```

---

## 👨‍💻 Autor

José Nobre