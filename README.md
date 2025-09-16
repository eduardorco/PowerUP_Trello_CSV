# 📊 Trello Data Export Power-Up

## Descrição

Este Power-Up permite exportar dados completos de quadros Trello em diversos formatos (JSON, CSV, Excel, HTML). É ideal para backup, análise de dados e relatórios.

## 🚀 Funcionalidades

### Exportação de Dados
- **Dados do Quadro**: Informações básicas, membros, etiquetas
- **Listas**: Todas as listas do quadro com posições
- **Cartões**: Informações completas incluindo:
  - Dados básicos (nome, descrição, posição)
  - Membros atribuídos
  - Etiquetas
  - Checklists
  - Anexos
  - Comentários
  - Datas de vencimento
- **Atividades**: Histórico completo de ações no quadro

### Formatos de Exportação
- **JSON**: Dados estruturados para integração com outras ferramentas
- **CSV**: Para análise em planilhas
- **Excel**: Formato .xlsx com múltiplas abas
- **HTML**: Relatório visual formatado

### Opções de Uso
- **Exportação Completa**: Todos os dados do quadro
- **Exportação Personalizada**: Selecione apenas os dados necessários
- **Exportação de Cartão Individual**: Botão em cada cartão

## 📋 Pré-requisitos

### 1. Criar Power-Up no Trello
1. Acesse [https://trello.com/power-ups/admin](https://trello.com/power-ups/admin)
2. Clique em "New" para criar um novo Power-Up
3. Preencha os campos obrigatórios:
   - **Nome**: "Trello Data Exporter"
   - **Workspace**: Selecione seu workspace
   - **iframe Connector URL**: URL onde o arquivo HTML está hospedado

### 2. Gerar API Key
1. No Power-Up criado, vá para a aba "API Key"
2. Clique em "Generate a new API Key"
3. Copie a API Key gerada

### 3. Gerar Token
1. Na mesma página da API Key, clique no link "Token"
2. Autorize o acesso
3. Copie o token gerado

### 4. Hospedar o Power-Up
Você pode usar qualquer uma dessas opções para hospedar o arquivo HTML:

#### GitHub Pages (Recomendado)
```bash
# 1. Crie um repositório no GitHub
# 2. Faça upload do arquivo HTML como index.html
# 3. Ative GitHub Pages nas configurações
# 4. Use a URL: https://seuusuario.github.io/seurepositorio/
```

#### Netlify
1. Acesse [netlify
