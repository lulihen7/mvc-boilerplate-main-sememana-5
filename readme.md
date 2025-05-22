# Boilerplate MVC em Node.js com PostgreSQL

Este projeto é um boilerplate básico para uma aplicação Node.js seguindo o padrão MVC (Model-View-Controller), utilizando PostgreSQL como banco de dados.

## Requisitos

- Node.js (versão X.X.X)
- PostgreSQL (versão X.X.X)

## Instalação

1. **Clonar o repositório:**

```bash
   git clone https://github.com/seu-usuario/seu-projeto.git
   cd seu-projeto
```

2. **Instalar as dependências:**
    
```bash
npm install
```
    
3. **Configurar o arquivo `.env`:**
    
Renomeie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente necessárias, como as configurações do banco de dados PostgreSQL.
    

Configuração do Banco de Dados
------------------------------

1. **Criar banco de dados:**
    
    Crie um banco de dados PostgreSQL com o nome especificado no seu arquivo `.env`.
    
2. **Executar o script SQL de inicialização:**
    
```bash
npm run init-db
```
    
Isso criará a tabela `users` no seu banco de dados PostgreSQL com UUID como chave primária e inserirá alguns registros de exemplo.
    

Funcionalidades
---------------

* **Padrão MVC:** Estrutura organizada em Model, View e Controller.
* **PostgreSQL:** Banco de dados relacional utilizado para persistência dos dados.
* **UUID:** Utilização de UUID como chave primária na tabela `users`.
* **Scripts com `nodemon`:** Utilização do `nodemon` para reiniciar automaticamente o servidor após alterações no código.
* **Testes:** Inclui estrutura básica para testes automatizados.

Scripts Disponíveis
-------------------

* `npm start`: Inicia o servidor Node.js.
* `npm run dev`: Inicia o servidor com `nodemon`, reiniciando automaticamente após alterações no código.
* `npm run test`: Executa os testes automatizados.
* `npm run test:coverage`: Executa os testes e gera um relatório de cobertura de código.

Estrutura de Diretórios
-----------------------

* **`config/`**: Configurações do banco de dados e outras configurações do projeto.
* **`controllers/`**: Controladores da aplicação (lógica de negócio).
* **`models/`**: Modelos da aplicação (definições de dados e interações com o banco de dados).
* **`routes/`**: Rotas da aplicação.
* **`tests/`**: Testes automatizados.
* **`views/`**: Views da aplicação (se aplicável).

Contribuição
------------

Contribuições são bem-vindas! Sinta-se à vontade para abrir um issue ou enviar um pull request.

Licença
-------

Este projeto está licenciado sob a Licença MIT.

atividade

### **1\. Papel de cada camada da arquitetura MVC e interação entre elas**

O **Model** representa os dados e regras de negócio, sendo responsável por acessar e manipular o banco de dados.  
 A **View** é a interface visual que exibe as informações ao usuário e recebe entradas (como formulários).  
 O **Controller** atua como intermediário: recebe as requisições da View, usa o Model para processar os dados e decide qual View ou resposta retornar.

Eles interagem da seguinte forma:  
 Usuário → View → Controller → Model → Controller → View → Usuário.

### **2\. Envio e recebimento de dados no formato JSON**

O projeto usa `express.json()` para interpretar requisições com corpo em JSON.  
 Uma rota que responde em JSON, por exemplo:

app.get('/api/usuarios', (req, res) \=\> {  
  res.json(\[{ id: 1, nome: 'Henrique' }\]);  
});

Essa rota retorna uma lista de usuários em formato JSON, útil para APIs que se comunicam com front-ends modernos ou apps.

### **3\. Importância do HTML com formulários e tabelas no navegador**

Formulários e tabelas em HTML permitem inserir e visualizar dados de forma simples e rápida.  
 São compatíveis com todos os navegadores, fáceis de implementar e ideais para interfaces administrativas ou protótipos.

### **4\. Por que essa estrutura ainda é útil com Node.js**

Mesmo com tecnologias modernas, HTML básico é útil em projetos internos, MVPs ou sistemas simples.  
 Evita a complexidade de um front-end separado e permite focar na lógica do back-end com eficiência.



Este README.md fornece uma visão geral clara do boilerplate, incluindo instruções de instalação, configuração do banco de dados, funcionalidades principais, scripts disponíveis, estrutura de diretórios, como contribuir e informações de licença. Certifique-se de personalizar as seções com detalhes específicos do seu projeto conforme necessário.
