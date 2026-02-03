# 🧪 API Tests - Automation Exercise (Postman Collection)

Este repositório contém uma collection do Postman para testes de API utilizando as APIs públicas do site **Automation Exercise**.

O objetivo do projeto é praticar:
- Testes de API (positivos e negativos)
- Validação de status code
- Validação de mensagens de resposta
- Uso de variáveis de ambiente
- Organização de collection para uso em pipeline (CI/CD)

---

## 📌 APIs testadas

A collection cobre os seguintes cenários:

1. Listar todos os produtos (GET)
2. Método inválido para produtos (POST)
3. Listar todas as marcas (GET)
4. Método inválido para marcas (PUT)
5. Buscar produtos (POST)
6. Buscar produtos sem parâmetro (POST)
7. Verificar login com dados válidos (POST)
8. Verificar login sem email (POST)
9. Método inválido para login (DELETE)
10. Verificar login com dados inválidos (POST)
11. Criar conta de usuário (POST)
12. Deletar conta de usuário (DELETE)
13. Atualizar conta de usuário (PUT)
14. Buscar detalhes do usuário por email (GET)

---

## 🛠️ Tecnologias utilizadas

- Postman
- Newman (execução via terminal / pipeline)
- API pública: https://automationexercise.com

---

## 📥 Como importar a collection

1. Abra o Postman
2. Clique em **Import**
3. Selecione o arquivo: collection.json
4. A collection será importada automaticamente  

---

## 🌎 Configuração do Environment

Crie um environment no Postman com as seguintes variáveis:

| Variável        | Valor (exemplo)                     |
|----------------|-------------------------------------|
| base_url       | https://automationexercise.com/api  |
| email_login    | seu_email_teste@mail.com            |
| email_criado   | outro_email_teste@mail.com          |
| password       | sua_senha                           |

⚠️ **Importante:**  
Não versionar environments reais com dados sensíveis no GitHub.

---

## ▶️ Como executar no Postman

1. Selecione o environment criado  
2. Execute os requests individualmente  
ou  
3. Clique em **Run Collection**

---

## 💻 Executar via Newman (CLI)

Instalar o Newman:
```bash
npm install -g newman
```
Executar:
```bash
newman run collection.json \
--env-var "base_url=https://automationexercise.com/api" \
--env-var "email_login=seu_email@mail.com" \
--env-var "email_criado=outro_email@mail.com" \
--env-var "password=sua_senha"
```

## 🔐 Boas práticas de segurança

- Nenhuma credencial real está salva na collection
- As variáveis são configuradas via environment
- Em pipelines, os valores devem ser configurados como secrets
- A collection pode ser versionada sem risco

---

## 📈 Objetivo do projeto

Este projeto foi criado para fins de:
- Estudo de testes de API
- Treinamento com Postman
- Portfólio profissional em QA
- Simulação de execução em CI/CD

---

## 👩‍💻 Autora

Giovana<br>
Analista de Qualidade de Software

---
## 📄 Licença

Este projeto é apenas para fins educacionais.
