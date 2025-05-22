

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


