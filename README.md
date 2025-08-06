# 🚗 Consulta Tabela FIPE - Java + Spring Boot

Este projeto é uma aplicação de linha de comando que consome a [API pública da Tabela FIPE](https://deividfortuna.github.io/fipe/) para consultar preços de veículos (carros, motos e caminhões) diretamente no terminal. A aplicação foi desenvolvida com Java, utilizando Spring Boot, e faz uso das bibliotecas `HttpClient` e `Jackson` para consumo e deserialização de dados JSON.

---

## 📌 Funcionalidades

- Escolha entre Carro, Moto ou Caminhão
- Lista todas as marcas disponíveis
- Filtra e exibe os modelos da marca selecionada
- Busca modelos pelo nome
- Lista os anos disponíveis para um modelo
- Exibe os detalhes e valores para cada ano de fabricação

---

## 💻 Tecnologias utilizadas

- Java 17+
- Spring Boot
- Maven
- HTTP Client (Java 11+)
- Jackson (para conversão JSON)
- API pública Tabela FIPE
- IntelliJ IDEA ou VS Code (sugestão de IDEs)

---

## 📁 Estrutura do projeto

```
tabela-fipe/
├── src/
│   ├── main/
│   │   ├── java/br/com/alura/tabelaFipe/
│   │   │   ├── model/
│   │   │   │   ├── Dados.java
│   │   │   │   ├── Modelos.java
│   │   │   │   └── Veiculo.java
│   │   │   ├── principal/
│   │   │   │   └── Principal.java
│   │   │   ├── service/
│   │   │   │   ├── ConsumoApi.java
│   │   │   │   ├── ConverteDados.java
│   │   │   │   └── IConverteDados.java
│   │   │   └── TabelaFipeApplication.java
│   └── resources/
│       └── application.properties
├── test/
│   └── java/br/com/alura/tabelaFipe/
│       └── TabelaFipeApplicationTests.java
├── pom.xml
└── README.md
```

---

## ▶️ Como executar o projeto

### 1. Pré-requisitos

- Java 17+
- Maven 3.8+
- Git (opcional, para clonar o projeto)

### 2. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/tabela-fipe.git
cd tabela-fipe
```

### 3. Executar via terminal

```bash
./mvnw spring-boot:run
```

Ou, se estiver no Windows:

```bash
mvnw.cmd spring-boot:run
```

---

## 🧪 Exemplo de uso

```
===== Opções =====
Carro
Moto
Caminhão

Digite uma das opções para consulta:
carro

{json das marcas...}
[001] - Fiat
[002] - Ford
[003] - Chevrolet

Informe o código da marca para consulta:
001

Modelos dessa marca:
[01001] - Uno
[01002] - Palio

Digite um trecho do nome do carro a ser buscado:
uno

Modelos filtrados:
[01001] - Uno

Digite o código do modelo:
01001

Todos os veículos filtrados com avaliação por ano:
Uno 2022 - R$ 25.000
Uno 2021 - R$ 23.500
...
```

---

## 📦 API utilizada

Esta aplicação utiliza a API pública da FIPE:

🔗 [https://parallelum.com.br/fipe/api/v1](https://parallelum.com.br/fipe/api/v1)

Documentação da API: [https://deividfortuna.github.io/fipe/](https://deividfortuna.github.io/fipe/)

---
