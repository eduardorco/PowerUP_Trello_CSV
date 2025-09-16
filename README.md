# 🚀 Setup Simples - Power-Up Extrator Trello

## Passos Rápidos (5 minutos)

### 1. Hospedar o Arquivo no GitHub

1. **Criar repositório no GitHub:**
   - Acesse [github.com](https://github.com)
   - Clique em "New repository"
   - Nome: `trello-extractor`
   - Marque "Public"
   - Marque "Add a README file"
   - Clique "Create repository"

2. **Adicionar o arquivo:**
   - No repositório criado, clique "Add file" > "Create new file"
   - Nome do arquivo: `index.html`
   - Cole todo o conteúdo do arquivo HTML que criei
   - Clique "Commit new file"

3. **Ativar GitHub Pages:**
   - Vá em "Settings" do repositório
   - No menu lateral, clique "Pages"
   - Em "Source", selecione "Deploy from a branch"
   - Branch: `main`
   - Folder: `/ (root)`
   - Clique "Save"
   - Aguarde alguns minutos e copie a URL: `https://seuusuario.github.io/trello-extractor`

### 2. Criar Power-Up no Trello

1. **Acesse o admin do Trello:**
   - Vá para [trello.com/power-ups/admin](https://trello.com/power-ups/admin)
   - Clique "New"

2. **Preencha os campos:**
   - **Name:** `Trello Data Extractor`
   - **Workspace:** Selecione seu workspace
   - **iframe Connector URL:** `https://seuusuario.github.io/trello-extractor`
   - Clique "Create"

3. **Configurar capabilities:**
   - No Power-Up criado, vá para "Capabilities"
   - Ative apenas: `board-buttons`
   - Salve as alterações

### 3. Testar o Power-Up

1. **Ir para um quadro:**
   - Abra qualquer quadro Trello
   - Clique "Power-Ups" no menu
   - Procure "Trello Data Extractor"
   - Clique "Enable"

2. **Usar o extrator:**
   - Você verá um botão "Extrair Dados" no header do quadro
   - Clique nele para abrir a interface
   - Cole uma URL de quadro público (ex: `https://trello.com/b/dQHqCohZ/trello-platform-changelog`)
   - Clique "Extrair Dados"
   - Faça download do JSON

## 📋 URLs de Quadros Públicos para Testar

- **Trello Platform Changes:** `https://trello.com/b/dQHqCohZ/trello-platform-changelog`
- **Trello Development Board:** `https://trello.com/b/cI66RoQS/trello-development-public-board`

## 🔧 Solução de Problemas

### Power-Up não aparece
- Verifique se a URL do GitHub Pages está correta
- Aguarde alguns minutos para o GitHub Pages ativar
- Teste se a URL funciona no navegador

### Erro "Board not found"
- Verifique se o quadro é público
- Confirme se a URL está no formato correto
- Teste com os exemplos fornecidos

### Botão não funciona
- Abra o console do navegador (F12)
- Veja se há erros JavaScript
- Verifique se o Power-Up foi habilitado no quadro

## 🎯 Funcionalidades

✅ **Extrai quadros públicos** sem necessidade de API Key  
✅ **Download em JSON** estruturado  
✅ **Interface simples** e intuitiva  
✅ **Seleção de dados** personalizável  
✅ **Funciona em qualquer quadro** público  

## 📊 Dados Extraídos

- **Quadro:** Nome, descrição, configurações
- **Listas:** Todas as listas com posições
- **Cartões:** Dados completos incluindo descrições, checklists, anexos
- **Membros:** Lista de usuários do quadro
- **Etiquetas:** Todas as labels configuradas
- **Atividades:** Histórico de ações (últimas 1000)

## 🔄 Para Atualizar

1. Edite o arquivo `index.html` no GitHub
2. Commit as mudanças
3. O Power-Up será atualizado automaticamente

---

**Pronto!** Agora você tem um Power-Up funcional para extrair dados de quadros públicos do Trello! 🎉
