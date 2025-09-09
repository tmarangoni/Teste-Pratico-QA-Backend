  TESTE AUTOMATIZADO (BACK-END)
  
Contexto:
Você está testando um serviço de pedidos em uma API RESTful. Os dados devem ser validados, testados em encadeamento e cobrir comportamentos esperados e não esperados.
Plataforma-alvo para testes:

Use a API pública: https://fakerestapi.azurewebsites.net/index.html
Desafio:
Implemente testes que façam o seguinte:
1.	Criar um novo Book via POST /api/v1/Books com os seguintes dados:
o	Title: “Test Automation Advanced”
o	Description: “Book created via automated test”
o	PageCount: 450
o	PublishDate: data atual no formato ISO
2.	Recuperar esse mesmo book usando o GET /api/v1/Books/{id} e validar:
o	Se os dados batem com o enviado
o	Se o id retornado é sequencial (opcional)
3.	Alterar o título do livro usando PUT, mantendo os demais dados.
4.	Tentar deletar um ID inexistente e validar o retorno de erro esperado.
5.	Tentar criar um book inválido com PageCount: -5 e validar se há validação server-side.
6.	Automatize todos os testes com:
o	Suíte organizada por arquivos ou classes
o	Fixture de dados reutilizável
o	Geração automática de dados dinâmicos (faker, uuid, etc.)




# 🧪 Instalação do Ambiente
 - Instalar Newman HTML+
```bash
npm install -g newman-reporter-htmlextra
```
# ✅ Execução dos Testes + Geração do relatório
```bash
newman run book_api_collection.json -r htmlextra
```
- Relatório será gerado na mesma pasta em que o arquivo .json da collection de testes está localizado