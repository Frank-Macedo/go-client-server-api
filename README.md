# Client-Server-API

Este repositório contém um desafio de implementação de uma API cliente-servidor em Go. O objetivo é consumir uma cotação de dólar (USD/BRL) de um endpoint externo e armazenar os dados no banco de dados com controle de timeout.

---

## Estrutura do Projeto

```
Client-Server-Api/
├── client/              # Cliente HTTP que consome a API externa de cotação
├── server/              # Servidor com endpoints e persistência de dados
│   ├── model/           # Modelos de dados (Cotacao, CotacaoDB)
│   ├── repository/      # Repositório com GORM (SQLite, PostgreSQL, MySQL)
│   ├── service/         # Regras de negócio
│   └── main.go          # Inicializa servidor e banco de dados
├── go.mod
└── README.md
```

---

## Funcionalidades

* Consulta de cotação USD/BRL de uma API externa
* Salvamento dos dados no banco de dados SQLite usando GORM
* Timeout de 10ms para operações de escrita no banco
* Projeto modular com separação clara de responsabilidades

---

## Tecnologias

* **Go 1.20+**
* **GORM** (ORM para Go)
* **SQLite** (banco de dados local)
* **Context API** para controle de timeout

---

## Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/seu-usuario/client-server-api.git
   cd client-server-api
   ```

2. Execute o servidor:

   ```bash
   cd server
   go run main.go
   ```

3. Em outro terminal, execute o cliente:

   ```bash
   cd ../client
   go run main.go
   ```

---

## Observações

* O banco de dados `cotacoes.db` será criado automaticamente ao iniciar o servidor.
* O projeto pode ser adaptado para usar PostgreSQL ou MySQL alterando o driver na configuração.

---

## Autor

Desenvolvido como parte de um desafio de prática com Go e APIs REST.

---

Se desejar contribuir, fique à vontade para abrir um PR ou criar issues!
# go-client-server-api
