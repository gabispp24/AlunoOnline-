# AlunoOnline

## 1. Introdução

A **Aluno Online API** é uma aplicação REST desenvolvida com Spring Boot que tem como finalidade gerenciar informações acadêmicas de forma simples e eficiente. O sistema permite manipular dados de alunos e professores por meio de operações básicas de um CRUD (Create, Read, Update, Delete).

O projeto foi estruturado seguindo boas práticas de organização em camadas, facilitando manutenção, escalabilidade e entendimento do código.

---

## 2. Finalidade do Projeto

A API foi criada para disponibilizar serviços HTTP capazes de:

* cadastrar novos alunos e professores;
* consultar todos os registros existentes;
* buscar informações específicas por ID;
* atualizar dados previamente cadastrados;
* excluir registros do sistema.

---

## 3. Tecnologias e Ferramentas

As principais tecnologias utilizadas no desenvolvimento foram:

* Java (Jakarta EE)
* Spring Boot
* Spring Web
* Spring Data JPA
* Hibernate
* Lombok
* Maven

Essas ferramentas permitem criar uma aplicação robusta com menor quantidade de código repetitivo e maior produtividade.

---

## 4. Organização do Projeto

A estrutura do sistema está organizada da seguinte forma:

```
src/main/java/br/com/alunoonline/api/
│
├── ApiApplication.java
│
├── controller/
│   ├── AlunoController.java
│   └── ProfessorController.java
│
├── model/
│   ├── Aluno.java
│   └── Professor.java
│
├── repository/
│   ├── AlunoRepository.java
│   └── ProfessorRepository.java
│
└── service/
    ├── AlunoService.java
    └── ProfessorService.java
```

Cada camada possui uma responsabilidade específica, garantindo melhor separação de interesses.

---

## 5. Arquitetura da Aplicação

O sistema segue o padrão de arquitetura em camadas:

* **Controller:** responsável por receber requisições HTTP e retornar respostas ao cliente.
* **Service:** contém as regras de negócio e validações.
* **Repository:** realiza a comunicação com o banco de dados.
* **Model:** representa as entidades do sistema.

### Fluxo de Funcionamento

```
Cliente → Controller → Service → Repository → Banco de Dados
```

---

## 6. Entidades do Sistema

### Aluno

Representa os estudantes cadastrados na aplicação.

| Campo        | Tipo   |
| ------------ | ------ |
| id           | Long   |
| nomeCompleto | String |
| cpf          | String |
| email        | String |

---

### Professor

Representa os professores cadastrados.

| Campo        | Tipo   |
| ------------ | ------ |
| id           | Long   |
| nomeCompleto | String |
| cpf          | String |
| email        | String |

---

## 7. Camada de Serviço

### AlunoService

* Criar aluno
* Listar todos os alunos
* Buscar aluno por ID
* Atualizar aluno
* Remover aluno

### ProfessorService

* Criar professor
* Listar professores
* Buscar professor por ID
* Atualizar professor
* Remover professor

---

## 8. Endpoints Disponíveis

<img width="740" height="576" alt="image" src="https://github.com/user-attachments/assets/bd84b9be-85c9-4546-b766-d887816e1d32" />


---

## 9. Considerações Finais

Este projeto serve como uma base sólida para aplicações REST utilizando Spring Boot. A separação em camadas e o uso de ferramentas modernas tornam o sistema fácil de entender, evoluir e adaptar para cenários mais complexos, como autenticação, validação avançada e integração com outros serviços.
