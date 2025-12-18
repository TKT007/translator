# Tradutor PT ↔ EN

Tradutor com IA usando OpenAI API, hospedado na Vercel.

## Funcionalidades

- Tradução Português → Inglês e Inglês → Português
- Preserva capitalização, pontuação e formatação
- "escalar" sempre traduz como "scale" (não "climb")
- Botão grande de copiar
- API Key segura no backend

## Estrutura do Projeto

```
translator-vercel/
├── api/
│   └── translate.js      # Serverless function
├── public/
│   └── index.html        # Frontend
├── package.json
├── vercel.json
└── README.md
```

## Deploy na Vercel

### 1. Suba para o GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/SEU_USUARIO/translator-pt-en.git
git push -u origin main
```

### 2. Conecte na Vercel

1. Vá em [vercel.com](https://vercel.com)
2. Clique em "Add New Project"
3. Importe o repositório do GitHub
4. **IMPORTANTE:** Adicione a variável de ambiente:
   - Nome: `OPENAI_API_KEY`
   - Valor: `sk-...` (sua chave da OpenAI)
5. Clique em "Deploy"

### 3. Configure a API Key

Na Vercel, vá em:
- Settings → Environment Variables
- Adicione: `OPENAI_API_KEY` = sua chave

## Uso Local (Desenvolvimento)

```bash
npm install -g vercel
vercel env add OPENAI_API_KEY
vercel dev
```

Acesse: http://localhost:3000
