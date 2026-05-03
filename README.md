# 🚀 API REST - Gerenciamento de Clientes

Este projeto é uma API REST desenvolvida com **Spring Boot**, com o objetivo de gerenciar clientes e seus endereços de forma inteligente, utilizando integração com API externa de CEP.

---

## 📚 Tecnologias utilizadas

* Java 21
* Spring Boot 2.5.4
* Spring Data JPA
* H2 Database
* OpenFeign
* Swagger (Springdoc OpenAPI)
* Maven

---

## ⚙️ Funcionalidades

* ✅ Cadastrar cliente
* ✅ Buscar cliente por ID
* ✅ Listar todos os clientes
* ✅ Atualizar cliente
* ✅ Deletar cliente
* ✅ Integração com API ViaCEP (preenchimento automático de endereço)

---

## 🧠 Como funciona

Ao cadastrar um cliente, basta informar:

* Nome
* CEP

A aplicação automaticamente consulta a API ViaCEP e preenche os dados do endereço.

---

## 🔗 Endpoints principais

### 📌 Criar cliente

POST `/clientes`

```json
{
  "nome": "Luiz Filipe",
  "endereco": {
    "cep": "01001000"
  }
}
```

---

### 📌 Listar clientes

GET `/clientes`

---

### 📌 Buscar cliente por ID

GET `/clientes/{id}`

---

### 📌 Atualizar cliente

PUT `/clientes/{id}`

---

### 📌 Deletar cliente

DELETE `/clientes/{id}`

---

## 🗄️ Banco de dados

O projeto utiliza o banco em memória **H2**.

Acesse o console:

http://localhost:8080/h2-console

**Configuração padrão:**

* JDBC URL: `jdbc:h2:mem:testdb`
* User: `sa`
* Password: (vazio)

---

## 📄 Documentação da API

A documentação interativa está disponível via Swagger:

http://localhost:8080/swagger-ui.html

ou

http://localhost:8080/swagger-ui/

---

## ▶️ Como executar o projeto

1. Clone o repositório:

```bash
git clone https://github.com/Filipe062/seu-repositorio.git
```

2. Acesse a pasta:

```bash
cd seu-repositorio
```

3. Execute o projeto:

```bash
mvn spring-boot:run
```

4. Acesse:

```bash
http://localhost:8080
```

---

## 💡 Observações importantes

* Não é necessário enviar o endereço completo no cadastro.
* Apenas o CEP é suficiente.
* O sistema busca automaticamente os dados via API externa.

---

## 👨‍💻 Autor

**Luiz Filipe Ferreira Gonçalves**

* GitHub: https://github.com/Filipe062
* LinkedIn: https://www.linkedin.com/in/luiz-filipe-ferreira-gon%C3%A7alves-083b85334

---

## 🔥 Status do projeto

✅ Concluído
🚀 Pronto para integração com front-end (React)

---
