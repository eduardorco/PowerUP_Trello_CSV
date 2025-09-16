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
1. Acesse [netlify.com](https://netlify.com)
2. Arraste e solte o arquivo HTML
3. Obtenha a URL HTTPS automaticamente

#### Vercel
1. Acesse [vercel.com](https://vercel.com)
2. Faça deploy do projeto
3. Receba URL HTTPS automaticamente

## ⚙️ Configuração

### 1. Atualizar Credenciais no Código
No arquivo HTML, localize e atualize estas linhas:

```javascript
// Linha ~134 - Substitua pela sua API Key
appKey: 'SUA_API_KEY_AQUI',

// Função validateAuth (linha ~315) - Atualize com suas credenciais
API_KEY = 'SUA_API_KEY_REAL';
API_TOKEN = 'SEU_TOKEN_REAL';
BOARD_ID = 'ID_DO_QUADRO_ATUAL'; // Opcional: será detectado automaticamente
```

### 2. Configurar Capabilities no Power-Up
No admin do Power-Up, ative as seguintes capabilities:
- ✅ **board-buttons**: Para botão de exportação no quadro
- ✅ **card-buttons**: Para botão de exportação em cartões individuais

### 3. Configurar Domínios Permitidos
Na aba "API Key" do seu Power-Up, adicione o domínio onde está hospedando:
- Se GitHub Pages: `https://seuusuario.github.io`
- Se Netlify: `https://seuapp.netlify.app`
- Se Vercel: `https://seuapp.vercel.app`

## 🔧 Instalação Completa

### Passo 1: Criar e Configurar o Power-Up
```bash
# 1. Acesse https://trello.com/power-ups/admin
# 2. Clique em "New"
# 3. Preencha os dados:
Nome: Trello Data Exporter
Workspace: [Seu Workspace]
iframe Connector URL: [URL do seu HTML hospedado]
```

### Passo 2: Obter Credenciais
```bash
# No Power-Up criado:
# 1. Vá para aba "API Key"
# 2. Clique "Generate a new API Key"
# 3. Copie a API Key
# 4. Clique no link "Token"
# 5. Autorize e copie o Token
```

### Passo 3: Configurar o Código
```javascript
// Substitua no arquivo HTML:
const CONFIG = {
    API_KEY: 'sua_api_key_aqui',
    APP_NAME: 'Trello Data Exporter',
    VERSION: '1.0.0'
};
```

### Passo 4: Hospedar o Arquivo
#### Opção A: GitHub Pages
```bash
git clone https://github.com/seu-usuario/trello-exporter
cd trello-exporter
# Coloque o arquivo HTML como index.html
git add .
git commit -m "Adicionar Power-Up"
git push origin main
# Ative GitHub Pages nas configurações do repositório
```

#### Opção B: Netlify Drop
1. Vá para [netlify.com](https://netlify.com)
2. Arraste o arquivo HTML para a área de drop
3. Copie a URL gerada

### Passo 5: Testar o Power-Up
1. Vá para um quadro Trello
2. Clique em "Power-Ups" no menu do quadro
3. Procure por "Trello Data Exporter"
4. Clique em "Enable"
5. Verifique se o botão "Exportar Dados" aparece no header do quadro

## 📊 Como Usar

### Exportação Completa do Quadro
1. Clique no botão "Exportar Dados" no header do quadro
2. Escolha "Exportação Rápida" para exportar tudo em JSON
3. Ou personalize selecionando os dados desejados

### Exportação Personalizada
1. Selecione as opções de dados desejadas:
   - 🏠 **Dados do Quadro**: Informações, membros, etiquetas
   - 📋 **Listas**: Informações e posições
   - 🎯 **Cartões**: Básico, descrição, membros, etiquetas, checklists, anexos, comentários, datas
   - 📈 **Atividades**: Todas as ações ou apenas comentários

2. Escolha o formato de exportação:
   - **JSON**: Dados estruturados
   - **CSV**: Para planilhas
   - **Excel**: Arquivo .xlsx
   - **HTML**: Relatório visual

3. Clique em "Exportar Dados"

### Exportação de Cartão Individual
1. Abra qualquer cartão
2. Clique em "Exportar Cartão" na barra lateral
3. O cartão será exportado em JSON com todos os detalhes

## 🔒 Segurança e Privacidade

### Dados Processados Localmente
- ✅ Todos os dados são processados no navegador
- ✅ Nenhum dado é enviado para servidores externos
- ✅ API Key e Token ficam apenas no seu navegador

### Recomendações de Segurança
- 🔐 Use tokens com escopo limitado quando possível
- 🔐 Configure domínios permitidos na API Key
- 🔐 Revogue tokens não utilizados regularmente
- 🔐 Não compartilhe suas credenciais

## 📁 Estrutura dos Dados Exportados

### JSON Export
```json
{
  "board": {
    "basic": { /* Informações do quadro */ },
    "members": [ /* Lista de membros */ ],
    "labels": [ /* Etiquetas do quadro */ ]
  },
  "lists": [ /* Todas as listas */ ],
  "cards": [
    {
      "id": "card_id",
      "name": "Nome do Cartão",
      "desc": "Descrição",
      "idList": "list_id",
      "idMembers": ["member1", "member2"],
      "labels": [ /* Etiquetas do cartão */ ],
      "checklists": [ /* Checklists */ ],
      "attachments": [ /* Anexos */ ],
      "comments": [ /* Comentários */ ],
      "due": "2024-12-31T23:59:59.000Z"
    }
  ],
  "actions": [ /* Histórico de atividades */ ],
  "metadata": {
    "exportDate": "2024-01-15T10:30:00.000Z",
    "exportedBy": "Trello Data Export Power-Up",
    "selectedOptions": { /* Opções selecionadas */ }
  }
}
```

### CSV Export
Arquivo com colunas:
- ID, Nome, Lista, Descrição, Membros, Etiquetas, Data de Vencimento

### HTML Export
Relatório formatado com seções:
- 📊 Header com informações do quadro
- 🎯 Cartões agrupados por lista
- 👥 Lista de membros
- 📈 Atividades recentes

## 🐛 Solução de Problemas

### Erro: "Credenciais não configuradas"
**Solução**: Verifique se API_KEY e API_TOKEN estão corretos no código

### Erro: "invalid token"
**Solução**: Gere um novo token em https://trello.com/power-ups/admin

### Erro: "API rate limit exceeded"
**Solução**: O Trello limita requests. Aguarde alguns minutos e tente novamente

### Power-Up não aparece no quadro
**Soluções**:
1. Verifique se o iframe Connector URL está correto
2. Confirme que o arquivo está acessível via HTTPS
3. Verifique se as capabilities estão ativadas
4. Limpe o cache do navegador

### Botão não funciona
**Soluções**:
1. Abra o console do navegador (F12) para ver erros
2. Verifique se a API Key está configurada
3. Confirme que o Power-Up tem permissões no workspace

## 🔄 Versionamento e Updates

### Para atualizar o Power-Up:
1. Faça as alterações no arquivo HTML
2. Faça upload da nova versão
3. O Power-Up será atualizado automaticamente nos quadros

### Changelog
- **v1.0.0**: Versão inicial com exportação completa
- Funcionalidades: JSON, CSV, HTML, Excel export
- Suporte a exportação personalizada
- Exportação de cartões individuais

## 🤝 Contribuições

Para melhorar este Power-Up:
1. Faça um fork do projeto
2. Implemente melhorias
3. Teste em diferentes quadros
4. Submeta um pull request

## 📞 Suporte

Para suporte:
1. Verifique a seção "Solução de Problemas"
2. Consulte a documentação da API Trello
3. Visite os fóruns da comunidade Trello
4. Contate o suporte através de https://go.trello.com/dev-support

## 📄 Licença

Este Power-Up é fornecido "como está" para fins educacionais e de uso pessoal. Use por sua própria conta e risco.
