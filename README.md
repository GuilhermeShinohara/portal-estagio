# 🎓 Portal de Estágios

Sistema Full-Stack para gerenciamento de estágios, desenvolvido com Java e Spring Boot, que conecta estudantes e empresas por meio da publicação de vagas, candidaturas e acompanhamento de oportunidades.

## 📋 Sobre o Projeto

O Portal de Estágios foi desenvolvido com o objetivo de simular um ambiente real de recrutamento para programas de estágio, permitindo que empresas publiquem oportunidades e que estudantes encontrem vagas alinhadas às suas áreas de interesse.

O projeto aplica conceitos de desenvolvimento de software, modelagem de dados, arquitetura em camadas e construção de APIs REST, seguindo boas práticas de organização, validação e integridade dos dados.

---

## ✨ Principais Funcionalidades

* Cadastro e gerenciamento de empresas
* Cadastro e gerenciamento de estudantes
* Cadastro de áreas de interesse
* Publicação e gerenciamento de vagas de estágio
* Controle de inscrições em vagas
* Encerramento de vagas
* Filtros de pesquisa
* Paginação de resultados
* Validações de negócio
* Documentação da API com Swagger

---

## 🏗️ Arquitetura da Aplicação

A aplicação foi desenvolvida seguindo o padrão de arquitetura em camadas (Layered Architecture), promovendo separação de responsabilidades, escalabilidade e facilidade de manutenção.

### Camadas

#### Controller

Responsável por receber requisições HTTP e retornar respostas da API.

#### Service

Implementa as regras de negócio e validações da aplicação.

#### Repository

Realiza a comunicação com o banco de dados utilizando Spring Data JPA.

#### Model

Representa as entidades do domínio e seus relacionamentos.

#### Database

Persistência dos dados utilizando banco H2 em memória para ambiente de desenvolvimento.

#### Frontend

Interface web desenvolvida com HTML, CSS e JavaScript consumindo a API REST.

---

## 🗄️ Modelagem de Dados

### Entidades

* Empresa
* Estudante
* Vaga de Estágio
* Área
* Inscrição

### Relacionamentos

| Relacionamento        | Tipo |
| --------------------- | ---- |
| Empresa → Vaga        | 1:N  |
| Vaga ↔ Área           | N:M  |
| Estudante ↔ Área      | N:M  |
| Estudante → Inscrição | 1:N  |
| Vaga → Inscrição      | 1:N  |

A modelagem foi projetada para garantir integridade referencial e consistência dos dados, evitando operações que possam comprometer o relacionamento entre as entidades.

---

## ⚙️ Regras de Negócio

O sistema implementa diversas validações para garantir a qualidade dos dados:

* E-mail único para estudantes e empresas
* Matrícula única para estudantes
* Campos obrigatórios validados
* Proteção contra exclusões inconsistentes
* Validação de relacionamentos entre entidades
* Controle de status das vagas

---

## 🛠️ Tecnologias Utilizadas

### Backend

* Java 21
* Spring Boot 3.4.5
* Spring Data JPA
* Hibernate
* Maven
* H2 Database

### Frontend

* HTML5
* CSS3
* JavaScript (Vanilla JS)

### Ferramentas

* Swagger/OpenAPI
* Postman
* Git
* GitHub

---

## 📡 Endpoints da API

### Empresas

```http
GET    /api/empresas
GET    /api/empresas/{id}
POST   /api/empresas
PUT    /api/empresas/{id}
DELETE /api/empresas/{id}
```

### Estudantes

```http
GET    /api/estudantes
GET    /api/estudantes/{id}
POST   /api/estudantes
PUT    /api/estudantes/{id}
DELETE /api/estudantes/{id}
```

### Vagas

```http
GET    /api/vagas
GET    /api/vagas/{id}
POST   /api/vagas
PUT    /api/vagas/{id}
PATCH  /api/vagas/{id}/encerrar
DELETE /api/vagas/{id}
```

Recursos adicionais:

* Filtro por empresa
* Filtro por área
* Paginação

### Áreas

```http
GET    /api/areas
GET    /api/areas/{id}
POST   /api/areas
PUT    /api/areas/{id}
DELETE /api/areas/{id}
```

### Inscrições

```http
GET    /api/inscricoes
POST   /api/inscricoes
PATCH  /api/inscricoes/{id}
DELETE /api/inscricoes/{id}
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

* Java 21 ou superior
* Maven 3.9 ou superior
* Git

### Clonando o Repositório

```bash
git clone https://github.com/SEU-USUARIO/portal-estagio.git
```

```bash
cd portal-estagio
```

### Compilando o Projeto

```bash
mvn clean install
```

### Executando a Aplicação

```bash
mvn spring-boot:run
```

A aplicação estará disponível em:

```text
http://localhost:8080
```

---

## 📖 Documentação da API

Após iniciar a aplicação, a documentação Swagger poderá ser acessada através do navegador:

```text
http://localhost:8080/swagger-ui.html
```

ou

```text
http://localhost:8080/swagger-ui/index.html
```

---

## 🎯 Objetivos de Aprendizagem

Este projeto foi desenvolvido para consolidar conhecimentos em:

* Desenvolvimento de APIs REST
* Spring Boot
* Persistência de dados com JPA/Hibernate
* Modelagem de banco de dados relacional
* Arquitetura em camadas
* Regras de negócio e validações
* Integração Frontend e Backend
* Boas práticas de desenvolvimento de software

---

## 📌 Melhorias Futuras

* Autenticação e autorização com JWT
* Controle de perfis (Administrador, Empresa e Estudante)
* Upload de currículo
* Notificações por e-mail
* Banco de dados PostgreSQL
* Deploy em ambiente cloud
* Testes automatizados
* Dashboard administrativo

---

## 👨‍💻 Autor

Desenvolvido como projeto acadêmico para aplicação prática de conceitos de Engenharia de Software, Desenvolvimento Web e Banco de Dados.

**Guilherme Shinohara**
