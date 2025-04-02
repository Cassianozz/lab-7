# lab-7
🔹 Passo 1: Criar um Recurso do Azure Cognitive Search
Acesse o Portal do Azure.

Clique em "Criar um recurso" (+) e busque por "Azure Cognitive Search".

Preencha os campos:

Assinatura: Selecione sua assinatura.

Grupo de recursos: Crie ou selecione um existente.

Nome do serviço: Ex.: meu-search-service.

Localização: Escolha uma região (ex.: East US).

Tipo de preço: Selecione "Standard" (ou "Free" para testes).

Clique em "Revisar + Criar" e depois em "Criar".

🔹 Passo 2: Preparar os Dados para Indexação
O Azure Cognitive Search pode indexar dados de:

Blob Storage (PDFs, Word, Excel).

Banco de Dados SQL.

Cosmos DB.

Outras fontes via API.

📌 Exemplo usando Blob Storage (arquivos em um container):

Crie um Azure Storage Account (se ainda não tiver).

Faça upload dos documentos (PDFs, Word, etc.) em um Blob Container.

🔹 Passo 3: Criar um Índice de Pesquisa
No Azure Cognitive Search, vá para "Índices" > "+ Novo Índice".

Defina:

Nome do índice: Ex.: meu-indice.

Campos:

id (Chave, tipo Edm.String).

conteudo (Texto extraído, tipo Edm.String, searchable).

titulo (Opcional, tipo Edm.String, filtrable).

Salve o índice.

🔹 Passo 4: Configurar um Indexador (Conexão com os Dados)
Vá para "Indexadores" > "+ Novo Indexador".

Defina:

Nome: Ex.: meu-indexador.

Fonte de dados: Conecte ao Blob Storage ou outra origem.

Índice de destino: Selecione o índice criado (meu-indice).

Habilite "Habilitação de IA" (opcional, para extração de entidades, OCR, etc.).

Execute o indexador ("Executar").

🔹 Passo 5: Testar a Pesquisa
No painel do Azure Cognitive Search, vá para "Search Explorer".

Digite uma consulta (ex.: contrato AND 2024).

Veja os resultados em JSON ou em um visualizador amigável.
